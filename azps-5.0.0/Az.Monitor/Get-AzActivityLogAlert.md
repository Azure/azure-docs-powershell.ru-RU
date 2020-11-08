---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248609"
---
# <span data-ttu-id="d9cfe-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9cfe-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="d9cfe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cfe-103">Получает один или несколько ресурсов для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="d9cfe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9cfe-104">SYNTAX</span></span>

### <span data-ttu-id="d9cfe-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9cfe-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cfe-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9cfe-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9cfe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9cfe-107">DESCRIPTION</span></span>
<span data-ttu-id="d9cfe-108">Командлет **Get-AzActivityLogAlert** получает один или несколько ресурсов для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="d9cfe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9cfe-109">EXAMPLES</span></span>

### <span data-ttu-id="d9cfe-110">Пример 1: получение уведомлений журнала активности по ИДЕНТИФИКАТОРу подписки</span><span class="sxs-lookup"><span data-stu-id="d9cfe-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="d9cfe-111">Эта команда выводит список всех оповещений журнала активности для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="d9cfe-112">Пример 2: получение оповещений журнала активности для указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d9cfe-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="d9cfe-113">Эта команда перечисляет оповещения журнала активности для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="d9cfe-114">Пример 3: Получение оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="d9cfe-115">Эта команда перечисляет один (список, в котором есть один элемент) оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="d9cfe-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9cfe-116">PARAMETERS</span></span>

### <span data-ttu-id="d9cfe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cfe-117">-DefaultProfile</span></span>
<span data-ttu-id="d9cfe-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9cfe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9cfe-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9cfe-119">-Name</span></span>
<span data-ttu-id="d9cfe-120">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="d9cfe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9cfe-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9cfe-122">Имя группы ресурсов, в которой находится ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="d9cfe-123">Если имя не равно null или пустое, этот параметр должен содержать и не пустую строку.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="d9cfe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cfe-124">CommonParameters</span></span>
<span data-ttu-id="d9cfe-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cfe-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9cfe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cfe-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9cfe-127">INPUTS</span></span>

### <span data-ttu-id="d9cfe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9cfe-128">System.String</span></span>

## <span data-ttu-id="d9cfe-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9cfe-129">OUTPUTS</span></span>

### <span data-ttu-id="d9cfe-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="d9cfe-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="d9cfe-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9cfe-131">NOTES</span></span>

## <span data-ttu-id="d9cfe-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9cfe-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9cfe-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9cfe-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d9cfe-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9cfe-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="d9cfe-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9cfe-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="d9cfe-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d9cfe-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="d9cfe-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="d9cfe-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
