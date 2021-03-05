---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ec35304bf6c376747fa6f98e7fb5753293e579b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008552"
---
# <span data-ttu-id="4dc61-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4dc61-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="4dc61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc61-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc61-103">Получает политику advanced threat protection для учетной записи storage/zusDB.</span><span class="sxs-lookup"><span data-stu-id="4dc61-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="4dc61-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4dc61-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc61-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dc61-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc61-106">Он получает политику защиты от угроз для учетной записи `Get-AzSecurityAdvancedThreatProtection` хранения или защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="4dc61-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="4dc61-107">Чтобы использовать этот cmdlet, укажите параметр *ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="4dc61-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="4dc61-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4dc61-108">EXAMPLES</span></span>

### <span data-ttu-id="4dc61-109">Пример 1. Учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="4dc61-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="4dc61-110">Эта команда получает политику advanced threat protection для ИД `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4dc61-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="4dc61-111">Пример 2. Учетная запись КЛИМОВА</span><span class="sxs-lookup"><span data-stu-id="4dc61-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="4dc61-112">Эта команда получает политику advanced threat protection для ИД ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4dc61-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="4dc61-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc61-113">PARAMETERS</span></span>

### <span data-ttu-id="4dc61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc61-114">-DefaultProfile</span></span>
<span data-ttu-id="4dc61-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc61-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dc61-116">-ResourceId</span></span>
<span data-ttu-id="4dc61-117">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="4dc61-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc61-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc61-118">CommonParameters</span></span>
<span data-ttu-id="4dc61-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc61-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc61-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc61-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc61-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dc61-121">INPUTS</span></span>

### <span data-ttu-id="4dc61-122">System.String</span><span class="sxs-lookup"><span data-stu-id="4dc61-122">System.String</span></span>

## <span data-ttu-id="4dc61-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dc61-123">OUTPUTS</span></span>

### <span data-ttu-id="4dc61-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4dc61-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="4dc61-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4dc61-125">NOTES</span></span>

## <span data-ttu-id="4dc61-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dc61-126">RELATED LINKS</span></span>
