---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246288"
---
# <span data-ttu-id="3c7cc-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="3c7cc-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="3c7cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7cc-103">Получение журнала Smart Group</span><span class="sxs-lookup"><span data-stu-id="3c7cc-103">Gets smart group history</span></span>

## <span data-ttu-id="3c7cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c7cc-104">SYNTAX</span></span>

### <span data-ttu-id="3c7cc-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c7cc-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c7cc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c7cc-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c7cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7cc-107">DESCRIPTION</span></span>
<span data-ttu-id="3c7cc-108">Командлет **Get-AzSmartGroupHistory** получает журнал Smart Group.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="3c7cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c7cc-109">EXAMPLES</span></span>

### <span data-ttu-id="3c7cc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c7cc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="3c7cc-111">Возвращает сведения о журнале Smart Group.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-111">Gets smart group history details.</span></span>

## <span data-ttu-id="3c7cc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c7cc-112">PARAMETERS</span></span>

### <span data-ttu-id="3c7cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7cc-113">-DefaultProfile</span></span>
<span data-ttu-id="3c7cc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c7cc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c7cc-115">-InputObject</span></span>
<span data-ttu-id="3c7cc-116">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7cc-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="3c7cc-117">-SmartGroupId</span></span>
<span data-ttu-id="3c7cc-118">Уникальный идентификатор SmartGroupа/ResourceId of Alert.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7cc-119">CommonParameters</span></span>
<span data-ttu-id="3c7cc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c7cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7cc-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c7cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7cc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c7cc-122">INPUTS</span></span>

### <span data-ttu-id="3c7cc-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c7cc-123">None</span></span>

## <span data-ttu-id="3c7cc-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7cc-124">OUTPUTS</span></span>

### <span data-ttu-id="3c7cc-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="3c7cc-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="3c7cc-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c7cc-126">NOTES</span></span>

## <span data-ttu-id="3c7cc-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c7cc-127">RELATED LINKS</span></span>
