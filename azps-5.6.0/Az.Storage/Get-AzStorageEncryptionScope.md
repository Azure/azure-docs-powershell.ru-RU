---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: 02d91338063a1c06654fa30cbbf584a6f62ea34a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981523"
---
# <span data-ttu-id="e2af6-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e2af6-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="e2af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2af6-102">SYNOPSIS</span></span>
<span data-ttu-id="e2af6-103">Получите или забирать области шифрования из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e2af6-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="e2af6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2af6-104">SYNTAX</span></span>

### <span data-ttu-id="e2af6-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2af6-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2af6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e2af6-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2af6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2af6-107">DESCRIPTION</span></span>
<span data-ttu-id="e2af6-108">Для получения или перечисления областей шифрования из учетной записи хранения используется cmdlet **Get-AzStorageEncryptionScope.**</span><span class="sxs-lookup"><span data-stu-id="e2af6-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="e2af6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2af6-109">EXAMPLES</span></span>

### <span data-ttu-id="e2af6-110">Пример 1. Получите единую область шифрования</span><span class="sxs-lookup"><span data-stu-id="e2af6-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="e2af6-111">Эта команда получает одну область шифрования.</span><span class="sxs-lookup"><span data-stu-id="e2af6-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="e2af6-112">Пример 2. Список всех областей шифрования учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e2af6-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="e2af6-113">Эта команда содержит список всех областей шифрования учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e2af6-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="e2af6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2af6-114">PARAMETERS</span></span>

### <span data-ttu-id="e2af6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2af6-115">-DefaultProfile</span></span>
<span data-ttu-id="e2af6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2af6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2af6-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="e2af6-117">-EncryptionScopeName</span></span>
<span data-ttu-id="e2af6-118">Имя службы шифрования хранилищ Azure</span><span class="sxs-lookup"><span data-stu-id="e2af6-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2af6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2af6-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2af6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2af6-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2af6-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2af6-121">-StorageAccount</span></span>
<span data-ttu-id="e2af6-122">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e2af6-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2af6-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e2af6-123">-StorageAccountName</span></span>
<span data-ttu-id="e2af6-124">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e2af6-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2af6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2af6-125">CommonParameters</span></span>
<span data-ttu-id="e2af6-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2af6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2af6-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2af6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2af6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2af6-128">INPUTS</span></span>

### <span data-ttu-id="e2af6-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2af6-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e2af6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2af6-130">OUTPUTS</span></span>

### <span data-ttu-id="e2af6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e2af6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="e2af6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2af6-132">NOTES</span></span>

## <span data-ttu-id="e2af6-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2af6-133">RELATED LINKS</span></span>
