---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400111"
---
# <span data-ttu-id="a512e-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="a512e-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="a512e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a512e-102">SYNOPSIS</span></span>
<span data-ttu-id="a512e-103">Получает сведения из истории оповещений</span><span class="sxs-lookup"><span data-stu-id="a512e-103">Gets Alert History information</span></span>

## <span data-ttu-id="a512e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a512e-104">SYNTAX</span></span>

### <span data-ttu-id="a512e-105">ByAlertId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a512e-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a512e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a512e-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a512e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a512e-107">DESCRIPTION</span></span>
<span data-ttu-id="a512e-108">**Химлет Get-AzAlertObjectHistory** получает историю оповещений.</span><span class="sxs-lookup"><span data-stu-id="a512e-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="a512e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a512e-109">EXAMPLES</span></span>

### <span data-ttu-id="a512e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a512e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="a512e-111">Возвращает сведения о истории оповещений.</span><span class="sxs-lookup"><span data-stu-id="a512e-111">Gets alert history details.</span></span> 

## <span data-ttu-id="a512e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a512e-112">PARAMETERS</span></span>

### <span data-ttu-id="a512e-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="a512e-113">-AlertId</span></span>
<span data-ttu-id="a512e-114">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a512e-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="a512e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a512e-115">-DefaultProfile</span></span>
<span data-ttu-id="a512e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a512e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a512e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a512e-117">-InputObject</span></span>
<span data-ttu-id="a512e-118">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a512e-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="a512e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a512e-119">CommonParameters</span></span>
<span data-ttu-id="a512e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a512e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a512e-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a512e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a512e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a512e-122">INPUTS</span></span>

### <span data-ttu-id="a512e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a512e-123">None</span></span>

## <span data-ttu-id="a512e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a512e-124">OUTPUTS</span></span>

### <span data-ttu-id="a512e-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="a512e-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="a512e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a512e-126">NOTES</span></span>

## <span data-ttu-id="a512e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a512e-127">RELATED LINKS</span></span>
