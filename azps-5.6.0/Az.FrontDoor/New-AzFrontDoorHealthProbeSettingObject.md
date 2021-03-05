---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971016"
---
# <span data-ttu-id="cdabb-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="cdabb-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="cdabb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdabb-102">SYNOPSIS</span></span>
<span data-ttu-id="cdabb-103">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="cdabb-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="cdabb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cdabb-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdabb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdabb-105">DESCRIPTION</span></span>
<span data-ttu-id="cdabb-106">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="cdabb-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="cdabb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cdabb-107">EXAMPLES</span></span>

### <span data-ttu-id="cdabb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdabb-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="cdabb-109">Примечание. Параметр HealthProbeMethod не чувствителен к делу.</span><span class="sxs-lookup"><span data-stu-id="cdabb-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="cdabb-110">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="cdabb-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="cdabb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdabb-111">PARAMETERS</span></span>

### <span data-ttu-id="cdabb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdabb-112">-DefaultProfile</span></span>
<span data-ttu-id="cdabb-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdabb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdabb-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cdabb-114">-EnabledState</span></span>
<span data-ttu-id="cdabb-115">Следует ли включить проверку состояния на отношении backends, определенных в backendPools.</span><span class="sxs-lookup"><span data-stu-id="cdabb-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="cdabb-116">Службы здравоохранения можно отключить только в том случае, если в одном пуле включена одна включенная резервная проверка.</span><span class="sxs-lookup"><span data-stu-id="cdabb-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="cdabb-117">-HealthProbeMethod</span></span>
<span data-ttu-id="cdabb-118">Определяет, какой метод HTTP нужно использовать для настройки backends, определенных в backendPools.</span><span class="sxs-lookup"><span data-stu-id="cdabb-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cdabb-119">-IntervalInSeconds</span></span>
<span data-ttu-id="cdabb-120">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="cdabb-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="cdabb-121">Значение по умолчанию — 30</span><span class="sxs-lookup"><span data-stu-id="cdabb-121">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cdabb-122">-Name</span></span>
<span data-ttu-id="cdabb-123">Имя параметра "Здоровье".</span><span class="sxs-lookup"><span data-stu-id="cdabb-123">Health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-124">-Path</span><span class="sxs-lookup"><span data-stu-id="cdabb-124">-Path</span></span>
<span data-ttu-id="cdabb-125">Путь, который нужно использовать для проверки здоровья.</span><span class="sxs-lookup"><span data-stu-id="cdabb-125">The path to use for the health probe.</span></span>
<span data-ttu-id="cdabb-126">Значение по умолчанию: /</span><span class="sxs-lookup"><span data-stu-id="cdabb-126">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cdabb-127">-Protocol</span></span>
<span data-ttu-id="cdabb-128">Протоколная схема, используемая для этого стандартного значения по умолчанию — HTTP</span><span class="sxs-lookup"><span data-stu-id="cdabb-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdabb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdabb-129">CommonParameters</span></span>
<span data-ttu-id="cdabb-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdabb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdabb-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdabb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdabb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdabb-132">INPUTS</span></span>

### <span data-ttu-id="cdabb-133">Нет</span><span class="sxs-lookup"><span data-stu-id="cdabb-133">None</span></span>
## <span data-ttu-id="cdabb-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdabb-134">OUTPUTS</span></span>

### <span data-ttu-id="cdabb-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="cdabb-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="cdabb-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cdabb-136">NOTES</span></span>

## <span data-ttu-id="cdabb-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdabb-137">RELATED LINKS</span></span>

<span data-ttu-id="cdabb-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cdabb-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
