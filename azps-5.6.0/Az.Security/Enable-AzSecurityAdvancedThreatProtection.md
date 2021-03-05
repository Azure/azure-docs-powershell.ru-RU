---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986597"
---
# <span data-ttu-id="65466-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="65466-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="65466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65466-102">SYNOPSIS</span></span>
<span data-ttu-id="65466-103">Включает расширенные политики защиты от угроз для учетной записи хранения или защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="65466-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="65466-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65466-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65466-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65466-105">DESCRIPTION</span></span>
<span data-ttu-id="65466-106">Этот cmdlet включает политику защиты от угроз для учетной записи `Enable-AzSecurityAdvancedThreatProtection` хранения или защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="65466-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="65466-107">Чтобы использовать этот cmdlet, укажите параметр *ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="65466-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="65466-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65466-108">EXAMPLES</span></span>

### <span data-ttu-id="65466-109">Пример 1. Учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="65466-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="65466-110">Эта команда включает политику advanced threat protection для ИД `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65466-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="65466-111">Пример 2. Учетная запись КЛИМОВА</span><span class="sxs-lookup"><span data-stu-id="65466-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="65466-112">Эта команда включает политику advanced threat protection для ИД ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65466-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="65466-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65466-113">PARAMETERS</span></span>

### <span data-ttu-id="65466-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65466-114">-DefaultProfile</span></span>
<span data-ttu-id="65466-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65466-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65466-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65466-116">-ResourceId</span></span>
<span data-ttu-id="65466-117">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="65466-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="65466-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65466-118">-Confirm</span></span>
<span data-ttu-id="65466-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65466-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65466-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65466-120">-WhatIf</span></span>
<span data-ttu-id="65466-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65466-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65466-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65466-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65466-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65466-123">CommonParameters</span></span>
<span data-ttu-id="65466-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65466-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65466-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65466-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65466-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65466-126">INPUTS</span></span>

### <span data-ttu-id="65466-127">Нет</span><span class="sxs-lookup"><span data-stu-id="65466-127">None</span></span>

## <span data-ttu-id="65466-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65466-128">OUTPUTS</span></span>

### <span data-ttu-id="65466-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="65466-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="65466-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65466-130">NOTES</span></span>

## <span data-ttu-id="65466-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65466-131">RELATED LINKS</span></span>
