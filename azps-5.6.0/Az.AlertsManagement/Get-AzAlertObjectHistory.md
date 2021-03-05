---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 31b72f68151132fc4dca1bddd18c1a15b6a36f3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961016"
---
# <span data-ttu-id="3988d-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="3988d-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="3988d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3988d-102">SYNOPSIS</span></span>
<span data-ttu-id="3988d-103">Получает сведения из истории оповещений</span><span class="sxs-lookup"><span data-stu-id="3988d-103">Gets Alert History information</span></span>

## <span data-ttu-id="3988d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3988d-104">SYNTAX</span></span>

### <span data-ttu-id="3988d-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3988d-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3988d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3988d-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3988d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3988d-107">DESCRIPTION</span></span>
<span data-ttu-id="3988d-108">**Химлет Get-AzAlertObjectHistory** получает историю оповещений.</span><span class="sxs-lookup"><span data-stu-id="3988d-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="3988d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3988d-109">EXAMPLES</span></span>

### <span data-ttu-id="3988d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3988d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="3988d-111">Возвращает сведения о истории оповещений.</span><span class="sxs-lookup"><span data-stu-id="3988d-111">Gets alert history details.</span></span> 

## <span data-ttu-id="3988d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3988d-112">PARAMETERS</span></span>

### <span data-ttu-id="3988d-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="3988d-113">-AlertId</span></span>
<span data-ttu-id="3988d-114">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3988d-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="3988d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3988d-115">-DefaultProfile</span></span>
<span data-ttu-id="3988d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3988d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3988d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3988d-117">-InputObject</span></span>
<span data-ttu-id="3988d-118">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3988d-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="3988d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3988d-119">CommonParameters</span></span>
<span data-ttu-id="3988d-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3988d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3988d-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3988d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3988d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3988d-122">INPUTS</span></span>

### <span data-ttu-id="3988d-123">Нет</span><span class="sxs-lookup"><span data-stu-id="3988d-123">None</span></span>

## <span data-ttu-id="3988d-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3988d-124">OUTPUTS</span></span>

### <span data-ttu-id="3988d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="3988d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="3988d-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3988d-126">NOTES</span></span>

## <span data-ttu-id="3988d-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3988d-127">RELATED LINKS</span></span>
