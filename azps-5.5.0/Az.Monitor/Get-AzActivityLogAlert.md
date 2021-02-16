---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 6f171edc1bc9b3d5f4d1f2a5d3ec568fac42929f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398569"
---
# <span data-ttu-id="10e1a-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="10e1a-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="10e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="10e1a-103">Возвращает один или несколько ресурсов журнала действий.</span><span class="sxs-lookup"><span data-stu-id="10e1a-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="10e1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10e1a-104">SYNTAX</span></span>

### <span data-ttu-id="10e1a-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10e1a-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e1a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10e1a-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10e1a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10e1a-107">DESCRIPTION</span></span>
<span data-ttu-id="10e1a-108">Для **этого можно использовать один** или несколько ресурсов журнала действий.</span><span class="sxs-lookup"><span data-stu-id="10e1a-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="10e1a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10e1a-109">EXAMPLES</span></span>

### <span data-ttu-id="10e1a-110">Пример 1. Получать оповещения журнала действий по ИД подписки</span><span class="sxs-lookup"><span data-stu-id="10e1a-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="10e1a-111">Эта команда содержит все оповещения журнала действий для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="10e1a-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="10e1a-112">Пример 2. Получать оповещения журнала действий для данной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="10e1a-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="10e1a-113">Эта команда содержит список оповещений журнала действий для данной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10e1a-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="10e1a-114">Пример 3. Оповещение в журнале действий.</span><span class="sxs-lookup"><span data-stu-id="10e1a-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="10e1a-115">Эта команда содержит одно оповещение журнала действий (список с одним элементом).</span><span class="sxs-lookup"><span data-stu-id="10e1a-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="10e1a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10e1a-116">PARAMETERS</span></span>

### <span data-ttu-id="10e1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e1a-117">-DefaultProfile</span></span>
<span data-ttu-id="10e1a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10e1a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10e1a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="10e1a-119">-Name</span></span>
<span data-ttu-id="10e1a-120">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="10e1a-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e1a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e1a-121">-ResourceGroupName</span></span>
<span data-ttu-id="10e1a-122">Имя группы ресурсов, в которой находится оповещение.</span><span class="sxs-lookup"><span data-stu-id="10e1a-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="10e1a-123">Если имя не является пустым или пустым, этот параметр должен содержать непустую строку.</span><span class="sxs-lookup"><span data-stu-id="10e1a-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e1a-124">CommonParameters</span></span>
<span data-ttu-id="10e1a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e1a-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e1a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e1a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10e1a-127">INPUTS</span></span>

### <span data-ttu-id="10e1a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="10e1a-128">System.String</span></span>

## <span data-ttu-id="10e1a-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10e1a-129">OUTPUTS</span></span>

### <span data-ttu-id="10e1a-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="10e1a-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="10e1a-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10e1a-131">NOTES</span></span>

## <span data-ttu-id="10e1a-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10e1a-132">RELATED LINKS</span></span>

[<span data-ttu-id="10e1a-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="10e1a-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)


[<span data-ttu-id="10e1a-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="10e1a-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="10e1a-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="10e1a-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="10e1a-136">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="10e1a-136">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
