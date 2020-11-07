---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900610"
---
# <span data-ttu-id="c3e19-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="c3e19-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="c3e19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3e19-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e19-103">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c3e19-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="c3e19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3e19-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e19-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3e19-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e19-106">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c3e19-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="c3e19-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3e19-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e19-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3e19-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="c3e19-109">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c3e19-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="c3e19-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3e19-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e19-111">-DefaultProfile</span></span>
<span data-ttu-id="c3e19-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e19-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e19-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c3e19-113">-IntervalInSeconds</span></span>
<span data-ttu-id="c3e19-114">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c3e19-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="c3e19-115">Значение по умолчанию: 30</span><span class="sxs-lookup"><span data-stu-id="c3e19-115">Default value is 30</span></span>

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

### <span data-ttu-id="c3e19-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3e19-116">-Name</span></span>
<span data-ttu-id="c3e19-117">имя параметра проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c3e19-117">health probe setting name.</span></span>

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

### <span data-ttu-id="c3e19-118">-Path</span><span class="sxs-lookup"><span data-stu-id="c3e19-118">-Path</span></span>
<span data-ttu-id="c3e19-119">Путь, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c3e19-119">The path to use for the health probe.</span></span>
<span data-ttu-id="c3e19-120">По умолчанию —/</span><span class="sxs-lookup"><span data-stu-id="c3e19-120">Default is /</span></span>

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

### <span data-ttu-id="c3e19-121">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c3e19-121">-Protocol</span></span>
<span data-ttu-id="c3e19-122">Схема протоколов, используемая для этого значения по умолчанию для пробной проверки — HTTP</span><span class="sxs-lookup"><span data-stu-id="c3e19-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="c3e19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e19-123">CommonParameters</span></span>
<span data-ttu-id="c3e19-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3e19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e19-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e19-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e19-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3e19-126">INPUTS</span></span>

### <span data-ttu-id="c3e19-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c3e19-127">None</span></span>

## <span data-ttu-id="c3e19-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3e19-128">OUTPUTS</span></span>

### <span data-ttu-id="c3e19-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c3e19-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="c3e19-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3e19-130">NOTES</span></span>

## <span data-ttu-id="c3e19-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3e19-131">RELATED LINKS</span></span>

<span data-ttu-id="c3e19-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c3e19-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
