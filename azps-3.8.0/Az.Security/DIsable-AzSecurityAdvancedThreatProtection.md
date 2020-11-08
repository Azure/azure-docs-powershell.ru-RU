---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 28e8521a283362989ff3ebace2f1e0a3e32c17a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073480"
---
# <span data-ttu-id="c401f-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c401f-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="c401f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c401f-102">SYNOPSIS</span></span>
<span data-ttu-id="c401f-103">Отключение расширенной политики защиты от угроз для учетной записи хранения и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c401f-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="c401f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c401f-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c401f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c401f-105">DESCRIPTION</span></span>
<span data-ttu-id="c401f-106">`Disable-AzSecurityAdvancedThreatProtection`Командлет отключает политику защиты от угроз для учетной записи хранилища и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c401f-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="c401f-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="c401f-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="c401f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c401f-108">EXAMPLES</span></span>

### <span data-ttu-id="c401f-109">Пример 1: учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="c401f-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="c401f-110">Эта команда отключает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c401f-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="c401f-111">Пример 2: учетная запись CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c401f-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="c401f-112">Эта команда отключает расширенную политику защиты от угроз для идентификатора ресурса ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="c401f-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="c401f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c401f-113">PARAMETERS</span></span>

### <span data-ttu-id="c401f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c401f-114">-DefaultProfile</span></span>
<span data-ttu-id="c401f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c401f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c401f-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c401f-116">-ResourceId</span></span>
<span data-ttu-id="c401f-117">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="c401f-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c401f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c401f-118">-Confirm</span></span>
<span data-ttu-id="c401f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c401f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c401f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c401f-120">-WhatIf</span></span>
<span data-ttu-id="c401f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c401f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c401f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c401f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c401f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c401f-123">CommonParameters</span></span>
<span data-ttu-id="c401f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c401f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c401f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c401f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c401f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c401f-126">INPUTS</span></span>

### <span data-ttu-id="c401f-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c401f-127">None</span></span>

## <span data-ttu-id="c401f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c401f-128">OUTPUTS</span></span>

### <span data-ttu-id="c401f-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c401f-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="c401f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c401f-130">NOTES</span></span>

## <span data-ttu-id="c401f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c401f-131">RELATED LINKS</span></span>
