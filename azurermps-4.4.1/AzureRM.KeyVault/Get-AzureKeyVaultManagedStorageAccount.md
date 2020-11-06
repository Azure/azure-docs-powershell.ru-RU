---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 7bf6539aaf849177d6e9da1fd74bcbedc28c8763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567612"
---
# <span data-ttu-id="924a0-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="924a0-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="924a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="924a0-102">SYNOPSIS</span></span>
<span data-ttu-id="924a0-103">Получение управляемых учетных записей хранилища Azure для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="924a0-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="924a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="924a0-104">SYNTAX</span></span>

### <span data-ttu-id="924a0-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="924a0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="924a0-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="924a0-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="924a0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="924a0-107">DESCRIPTION</span></span>
<span data-ttu-id="924a0-108">Возвращает управляемую учетную запись хранилища Azure с основным хранилищем, если указано имя учетной записи, а ключи учетной записи управляются указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="924a0-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="924a0-109">Если имя учетной записи не указано, перечисляются все учетные записи, для которых управление ключами задается указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="924a0-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="924a0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="924a0-110">EXAMPLES</span></span>

### <span data-ttu-id="924a0-111">Пример 1: список всех учетных записей хранения с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="924a0-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="924a0-112">Выводит все учетные записи, для которых управление ключами является хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="924a0-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="924a0-113">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="924a0-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="924a0-114">Получение сведений об учетной записи хранения ключа управляемого хранилища для "mystorageaccount", если ее ключи управляются хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="924a0-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="924a0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="924a0-115">PARAMETERS</span></span>

### <span data-ttu-id="924a0-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="924a0-116">-AccountName</span></span>
<span data-ttu-id="924a0-117">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="924a0-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="924a0-118">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="924a0-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924a0-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="924a0-119">-VaultName</span></span>
<span data-ttu-id="924a0-120">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="924a0-120">Vault name.</span></span>
<span data-ttu-id="924a0-121">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="924a0-121">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924a0-122">-DefaultProfile</span></span>
<span data-ttu-id="924a0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="924a0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924a0-124">CommonParameters</span></span>
<span data-ttu-id="924a0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="924a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924a0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924a0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="924a0-127">INPUTS</span></span>

### <span data-ttu-id="924a0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="924a0-128">System.String</span></span>

## <span data-ttu-id="924a0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="924a0-129">OUTPUTS</span></span>

### <span data-ttu-id="924a0-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. KeyVault, Version = 2.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="924a0-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="924a0-131">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="924a0-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="924a0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="924a0-132">NOTES</span></span>

## <span data-ttu-id="924a0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="924a0-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

