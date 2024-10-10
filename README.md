import KeychainAccess

// Define the service name for your keychain items
let serviceName = "YourServiceName"

// Create a Keychain instance
let keychain = Keychain(service: serviceName)

// Save a password to the keychain
try keychain.set("yourPassword", key: "passwordKey")

// Retrieve the password from the keychain
if let password = try keychain.get("passwordKey") {
  print("Password: (password)")
} else {
  print("Password not found in keychain.")
}

// Update the password in the keychain
try keychain.set("newYourPassword", key: "passwordKey")

// Delete the password from the keychain
try keychain.remove("passwordKey")
