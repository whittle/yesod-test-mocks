# yesod-test-mocks

1. Modify your app so that any behaviors you want to mock will be
   accessed through actions that are part of the Application type.
2. Create a data type to hold your mocks for each spec.
3. Change imports of `Yesod.Test` to `Yesod.Test.Mocks`.
4. Change any references of `YesodExample site` to `YesodExample site
   mocks`.
5. In the set-up code for your specs, instead of providing a pair of
   (app, middleware), instead provide a triple of (app, middleware,
   emptyMocks).
6. When you set up your app for use in specs, instead of equipping the
   Application type with actions that really perform the actions,
   make them refer to your mocks structure, instead.
7. In your specs, set any mocks necessary before making requests.
8. (Optional) In your spec tear-down, check to make sure that your
   mocks were consumed.
