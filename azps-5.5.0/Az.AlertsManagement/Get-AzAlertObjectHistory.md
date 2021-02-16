---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226676"
---
# <span data-ttu-id="37969-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="37969-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="37969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37969-102">SYNOPSIS</span></span>
<span data-ttu-id="37969-103">Получает сведения из истории оповещений</span><span class="sxs-lookup"><span data-stu-id="37969-103">Gets Alert History information</span></span>

## <span data-ttu-id="37969-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37969-104">SYNTAX</span></span>

### <span data-ttu-id="37969-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37969-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37969-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37969-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37969-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37969-107">DESCRIPTION</span></span>
<span data-ttu-id="37969-108">**Химлет Get-AzAlertObjectHistory** получает историю оповещений.</span><span class="sxs-lookup"><span data-stu-id="37969-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="37969-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37969-109">EXAMPLES</span></span>

### <span data-ttu-id="37969-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37969-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="37969-111">Возвращает сведения о истории оповещений.</span><span class="sxs-lookup"><span data-stu-id="37969-111">Gets alert history details.</span></span> 

## <span data-ttu-id="37969-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37969-112">PARAMETERS</span></span>

### <span data-ttu-id="37969-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="37969-113">-AlertId</span></span>
<span data-ttu-id="37969-114">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="37969-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="37969-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37969-115">-DefaultProfile</span></span>
<span data-ttu-id="37969-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37969-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37969-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37969-117">-InputObject</span></span>
<span data-ttu-id="37969-118">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="37969-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="37969-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37969-119">CommonParameters</span></span>
<span data-ttu-id="37969-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37969-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37969-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37969-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37969-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37969-122">INPUTS</span></span>

### <span data-ttu-id="37969-123">Нет</span><span class="sxs-lookup"><span data-stu-id="37969-123">None</span></span>

## <span data-ttu-id="37969-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37969-124">OUTPUTS</span></span>

### <span data-ttu-id="37969-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="37969-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="37969-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37969-126">NOTES</span></span>

## <span data-ttu-id="37969-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37969-127">RELATED LINKS</span></span>
