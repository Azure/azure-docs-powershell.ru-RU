---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: deef0be93c3a80c0db9762907eb52cdc51da9ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729263"
---
# <span data-ttu-id="92d48-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="92d48-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="92d48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92d48-102">SYNOPSIS</span></span>
<span data-ttu-id="92d48-103">Включает расширенную политику защиты от угроз для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="92d48-103">Enables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="92d48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92d48-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d48-105">DESCRIPTION</span></span>
<span data-ttu-id="92d48-106">`Enable-AzSecurityAdvancedThreatProtection`Командлет включает политику protetion угроз для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="92d48-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="92d48-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="92d48-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="92d48-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92d48-108">EXAMPLES</span></span>

### <span data-ttu-id="92d48-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92d48-109">Example 1</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="92d48-110">Эта команда включает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="92d48-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="92d48-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92d48-111">PARAMETERS</span></span>

### <span data-ttu-id="92d48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d48-112">-DefaultProfile</span></span>
<span data-ttu-id="92d48-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92d48-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d48-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d48-114">-ResourceId</span></span>
<span data-ttu-id="92d48-115">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="92d48-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="92d48-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92d48-116">-Confirm</span></span>
<span data-ttu-id="92d48-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92d48-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d48-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d48-118">-WhatIf</span></span>
<span data-ttu-id="92d48-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92d48-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92d48-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92d48-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d48-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d48-121">CommonParameters</span></span>
<span data-ttu-id="92d48-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92d48-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d48-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d48-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d48-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92d48-124">INPUTS</span></span>

### <span data-ttu-id="92d48-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="92d48-125">None</span></span>

## <span data-ttu-id="92d48-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d48-126">OUTPUTS</span></span>

### <span data-ttu-id="92d48-127">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="92d48-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="92d48-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="92d48-128">NOTES</span></span>

## <span data-ttu-id="92d48-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92d48-129">RELATED LINKS</span></span>
