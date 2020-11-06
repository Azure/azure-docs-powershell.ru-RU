---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: 92c4ea23f54025fdf32821742896459587f605f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565424"
---
# <span data-ttu-id="3724c-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3724c-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="3724c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3724c-102">SYNOPSIS</span></span>
<span data-ttu-id="3724c-103">Удаление профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="3724c-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3724c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3724c-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3724c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3724c-105">DESCRIPTION</span></span>
<span data-ttu-id="3724c-106">Командлет **Remove-AzureRmLogProfile** удаляет профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="3724c-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="3724c-107">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="3724c-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="3724c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3724c-108">EXAMPLES</span></span>

## <span data-ttu-id="3724c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3724c-109">PARAMETERS</span></span>

### <span data-ttu-id="3724c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3724c-110">-DefaultProfile</span></span>
<span data-ttu-id="3724c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3724c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3724c-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3724c-112">-Name</span></span>
<span data-ttu-id="3724c-113">Указывает имя профиля, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3724c-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="3724c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3724c-114">-PassThru</span></span>
<span data-ttu-id="3724c-115">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="3724c-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3724c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3724c-116">-Confirm</span></span>
<span data-ttu-id="3724c-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3724c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3724c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3724c-118">-WhatIf</span></span>
<span data-ttu-id="3724c-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3724c-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3724c-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3724c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3724c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3724c-121">CommonParameters</span></span>
<span data-ttu-id="3724c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3724c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3724c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3724c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3724c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3724c-124">INPUTS</span></span>

### <span data-ttu-id="3724c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3724c-125">System.String</span></span>

## <span data-ttu-id="3724c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3724c-126">OUTPUTS</span></span>

### <span data-ttu-id="3724c-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3724c-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3724c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3724c-128">NOTES</span></span>

## <span data-ttu-id="3724c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3724c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3724c-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3724c-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="3724c-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3724c-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


