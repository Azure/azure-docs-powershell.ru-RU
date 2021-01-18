---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504882"
---
# <span data-ttu-id="149a6-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="149a6-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="149a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149a6-102">SYNOPSIS</span></span>
<span data-ttu-id="149a6-103">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="149a6-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="149a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="149a6-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="149a6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="149a6-105">DESCRIPTION</span></span>
<span data-ttu-id="149a6-106">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="149a6-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="149a6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="149a6-107">EXAMPLES</span></span>

### <span data-ttu-id="149a6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="149a6-108">Example 1</span></span>
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

<span data-ttu-id="149a6-109">Примечание. Параметр HealthProbeMethod не чувствителен к делу.</span><span class="sxs-lookup"><span data-stu-id="149a6-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="149a6-110">Создание объекта PSHealthProbeSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="149a6-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="149a6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="149a6-111">PARAMETERS</span></span>

### <span data-ttu-id="149a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149a6-112">-DefaultProfile</span></span>
<span data-ttu-id="149a6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="149a6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="149a6-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="149a6-114">-EnabledState</span></span>
<span data-ttu-id="149a6-115">Следует ли включить проверку здоровья на отношении backends, определенных в backendPools.</span><span class="sxs-lookup"><span data-stu-id="149a6-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="149a6-116">Службы здравоохранения можно отключить только в том случае, если в одном пуле включена одна включенная резервная проверка.</span><span class="sxs-lookup"><span data-stu-id="149a6-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="149a6-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="149a6-117">-HealthProbeMethod</span></span>
<span data-ttu-id="149a6-118">Определяет, какой метод HTTP нужно использовать для настройки backends, определенных в backendPools.</span><span class="sxs-lookup"><span data-stu-id="149a6-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="149a6-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="149a6-119">-IntervalInSeconds</span></span>
<span data-ttu-id="149a6-120">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="149a6-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="149a6-121">Значение по умолчанию — 30</span><span class="sxs-lookup"><span data-stu-id="149a6-121">Default value is 30</span></span>

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

### <span data-ttu-id="149a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="149a6-122">-Name</span></span>
<span data-ttu-id="149a6-123">Имя параметра "Здоровье".</span><span class="sxs-lookup"><span data-stu-id="149a6-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="149a6-124">-Path</span><span class="sxs-lookup"><span data-stu-id="149a6-124">-Path</span></span>
<span data-ttu-id="149a6-125">Путь, который нужно использовать для проверки здоровья.</span><span class="sxs-lookup"><span data-stu-id="149a6-125">The path to use for the health probe.</span></span>
<span data-ttu-id="149a6-126">Значение по умолчанию: /</span><span class="sxs-lookup"><span data-stu-id="149a6-126">Default is /</span></span>

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

### <span data-ttu-id="149a6-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="149a6-127">-Protocol</span></span>
<span data-ttu-id="149a6-128">Протоколная схема, используемая для этого стандартного значения по умолчанию HTTP</span><span class="sxs-lookup"><span data-stu-id="149a6-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="149a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149a6-129">CommonParameters</span></span>
<span data-ttu-id="149a6-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149a6-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="149a6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149a6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="149a6-132">INPUTS</span></span>

### <span data-ttu-id="149a6-133">Нет</span><span class="sxs-lookup"><span data-stu-id="149a6-133">None</span></span>
## <span data-ttu-id="149a6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="149a6-134">OUTPUTS</span></span>

### <span data-ttu-id="149a6-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="149a6-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="149a6-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="149a6-136">NOTES</span></span>

## <span data-ttu-id="149a6-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="149a6-137">RELATED LINKS</span></span>

<span data-ttu-id="149a6-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="149a6-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
