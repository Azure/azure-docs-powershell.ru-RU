---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226673"
---
# <span data-ttu-id="1463d-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="1463d-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="1463d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1463d-102">SYNOPSIS</span></span>
<span data-ttu-id="1463d-103">Получает историю смарт-групп</span><span class="sxs-lookup"><span data-stu-id="1463d-103">Gets smart group history</span></span>

## <span data-ttu-id="1463d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1463d-104">SYNTAX</span></span>

### <span data-ttu-id="1463d-105">BySmartGroupId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1463d-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1463d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1463d-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1463d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1463d-107">DESCRIPTION</span></span>
<span data-ttu-id="1463d-108">**Для получения истории смарт-групп возвращается cmdlet Get-AzSmartGroupHistory.**</span><span class="sxs-lookup"><span data-stu-id="1463d-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="1463d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1463d-109">EXAMPLES</span></span>

### <span data-ttu-id="1463d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1463d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="1463d-111">Возвращает сведения о истории смарт-групп.</span><span class="sxs-lookup"><span data-stu-id="1463d-111">Gets smart group history details.</span></span>

## <span data-ttu-id="1463d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1463d-112">PARAMETERS</span></span>

### <span data-ttu-id="1463d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1463d-113">-DefaultProfile</span></span>
<span data-ttu-id="1463d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1463d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1463d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1463d-115">-InputObject</span></span>
<span data-ttu-id="1463d-116">Входной объект из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1463d-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="1463d-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="1463d-117">-SmartGroupId</span></span>
<span data-ttu-id="1463d-118">Уникальный идентификатор в оповещении SmartGroup или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1463d-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="1463d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1463d-119">CommonParameters</span></span>
<span data-ttu-id="1463d-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1463d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1463d-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1463d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1463d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1463d-122">INPUTS</span></span>

### <span data-ttu-id="1463d-123">Нет</span><span class="sxs-lookup"><span data-stu-id="1463d-123">None</span></span>

## <span data-ttu-id="1463d-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1463d-124">OUTPUTS</span></span>

### <span data-ttu-id="1463d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="1463d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="1463d-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1463d-126">NOTES</span></span>

## <span data-ttu-id="1463d-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1463d-127">RELATED LINKS</span></span>
