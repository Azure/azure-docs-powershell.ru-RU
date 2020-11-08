---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244944"
---
# <span data-ttu-id="0573d-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0573d-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="0573d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0573d-102">SYNOPSIS</span></span>
<span data-ttu-id="0573d-103">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="0573d-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0573d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0573d-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0573d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0573d-105">DESCRIPTION</span></span>
<span data-ttu-id="0573d-106">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="0573d-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0573d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0573d-107">EXAMPLES</span></span>

### <span data-ttu-id="0573d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0573d-108">Example 1</span></span>
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

<span data-ttu-id="0573d-109">Примечание. параметр HealthProbeMethod не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0573d-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="0573d-110">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="0573d-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0573d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0573d-111">PARAMETERS</span></span>

### <span data-ttu-id="0573d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0573d-112">-DefaultProfile</span></span>
<span data-ttu-id="0573d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0573d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0573d-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0573d-114">-EnabledState</span></span>
<span data-ttu-id="0573d-115">Следует ли включать проверки работоспособности в соответствии с последовательностью, определенной в backendPools.</span><span class="sxs-lookup"><span data-stu-id="0573d-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="0573d-116">Проверка работоспособности может быть отключена только в том случае, если имеется один включенный сервер в одном включенном пуле баз данных.</span><span class="sxs-lookup"><span data-stu-id="0573d-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="0573d-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="0573d-117">-HealthProbeMethod</span></span>
<span data-ttu-id="0573d-118">Настраивает метод HTTP, используемый для проверки поbackendPoolsов, заданных в разделе "проверяются".</span><span class="sxs-lookup"><span data-stu-id="0573d-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="0573d-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0573d-119">-IntervalInSeconds</span></span>
<span data-ttu-id="0573d-120">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="0573d-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="0573d-121">Значение по умолчанию: 30</span><span class="sxs-lookup"><span data-stu-id="0573d-121">Default value is 30</span></span>

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

### <span data-ttu-id="0573d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0573d-122">-Name</span></span>
<span data-ttu-id="0573d-123">Имя параметра проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="0573d-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="0573d-124">-Path</span><span class="sxs-lookup"><span data-stu-id="0573d-124">-Path</span></span>
<span data-ttu-id="0573d-125">Путь, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="0573d-125">The path to use for the health probe.</span></span>
<span data-ttu-id="0573d-126">По умолчанию —/</span><span class="sxs-lookup"><span data-stu-id="0573d-126">Default is /</span></span>

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

### <span data-ttu-id="0573d-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="0573d-127">-Protocol</span></span>
<span data-ttu-id="0573d-128">Схема протоколов, используемая для этого значения по умолчанию для пробной проверки — HTTP</span><span class="sxs-lookup"><span data-stu-id="0573d-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="0573d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0573d-129">CommonParameters</span></span>
<span data-ttu-id="0573d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0573d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0573d-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0573d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0573d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0573d-132">INPUTS</span></span>

### <span data-ttu-id="0573d-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="0573d-133">None</span></span>
## <span data-ttu-id="0573d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0573d-134">OUTPUTS</span></span>

### <span data-ttu-id="0573d-135">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0573d-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="0573d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0573d-136">NOTES</span></span>

## <span data-ttu-id="0573d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0573d-137">RELATED LINKS</span></span>

<span data-ttu-id="0573d-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0573d-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
