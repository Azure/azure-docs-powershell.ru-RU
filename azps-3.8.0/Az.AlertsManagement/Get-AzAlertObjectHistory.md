---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065674"
---
# <span data-ttu-id="9c12a-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="9c12a-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="9c12a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c12a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c12a-103">Получение сведений о журнале оповещений</span><span class="sxs-lookup"><span data-stu-id="9c12a-103">Gets Alert History information</span></span>

## <span data-ttu-id="9c12a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c12a-104">SYNTAX</span></span>

### <span data-ttu-id="9c12a-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c12a-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c12a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c12a-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c12a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c12a-107">DESCRIPTION</span></span>
<span data-ttu-id="9c12a-108">Командлет **Get-AzAlertObjectHistory** получает историю оповещений.</span><span class="sxs-lookup"><span data-stu-id="9c12a-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="9c12a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c12a-109">EXAMPLES</span></span>

### <span data-ttu-id="9c12a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c12a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="9c12a-111">Возвращает сведения о журнале оповещений.</span><span class="sxs-lookup"><span data-stu-id="9c12a-111">Gets alert history details.</span></span> 

## <span data-ttu-id="9c12a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c12a-112">PARAMETERS</span></span>

### <span data-ttu-id="9c12a-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="9c12a-113">-AlertId</span></span>
<span data-ttu-id="9c12a-114">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="9c12a-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c12a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c12a-115">-DefaultProfile</span></span>
<span data-ttu-id="9c12a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c12a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c12a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c12a-117">-InputObject</span></span>
<span data-ttu-id="9c12a-118">Объект ввода из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9c12a-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="9c12a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c12a-119">CommonParameters</span></span>
<span data-ttu-id="9c12a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c12a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c12a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c12a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c12a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c12a-122">INPUTS</span></span>

### <span data-ttu-id="9c12a-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c12a-123">None</span></span>

## <span data-ttu-id="9c12a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c12a-124">OUTPUTS</span></span>

### <span data-ttu-id="9c12a-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="9c12a-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="9c12a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c12a-126">NOTES</span></span>

## <span data-ttu-id="9c12a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c12a-127">RELATED LINKS</span></span>
