---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249144"
---
# <span data-ttu-id="f1627-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f1627-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f1627-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1627-102">SYNOPSIS</span></span>
<span data-ttu-id="f1627-103">Включает расширенную политику защиты от угроз для учетной записи хранения и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f1627-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="f1627-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1627-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1627-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1627-105">DESCRIPTION</span></span>
<span data-ttu-id="f1627-106">`Enable-AzSecurityAdvancedThreatProtection`Командлет включает политику защиты от угроз для учетной записи хранилища и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f1627-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="f1627-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f1627-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f1627-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1627-108">EXAMPLES</span></span>

### <span data-ttu-id="f1627-109">Пример 1: учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="f1627-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f1627-110">Эта команда включает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="f1627-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="f1627-111">Пример 2: учетная запись CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f1627-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="f1627-112">Эта команда включает расширенную политику защиты от угроз для идентификатора ресурса ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="f1627-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="f1627-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1627-113">PARAMETERS</span></span>

### <span data-ttu-id="f1627-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1627-114">-DefaultProfile</span></span>
<span data-ttu-id="f1627-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1627-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1627-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1627-116">-ResourceId</span></span>
<span data-ttu-id="f1627-117">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="f1627-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f1627-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1627-118">-Confirm</span></span>
<span data-ttu-id="f1627-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1627-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1627-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1627-120">-WhatIf</span></span>
<span data-ttu-id="f1627-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1627-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1627-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1627-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1627-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1627-123">CommonParameters</span></span>
<span data-ttu-id="f1627-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1627-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1627-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1627-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1627-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1627-126">INPUTS</span></span>

### <span data-ttu-id="f1627-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1627-127">None</span></span>

## <span data-ttu-id="f1627-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1627-128">OUTPUTS</span></span>

### <span data-ttu-id="f1627-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f1627-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f1627-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1627-130">NOTES</span></span>

## <span data-ttu-id="f1627-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1627-131">RELATED LINKS</span></span>