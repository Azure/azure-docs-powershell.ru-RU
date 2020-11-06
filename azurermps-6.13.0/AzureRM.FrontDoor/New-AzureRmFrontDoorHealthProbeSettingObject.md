---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564527"
---
# <span data-ttu-id="ed0b8-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="ed0b8-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="ed0b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0b8-103">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed0b8-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed0b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed0b8-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed0b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0b8-106">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed0b8-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="ed0b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed0b8-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed0b8-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="ed0b8-109">Создание объекта PSHealthProbeSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed0b8-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="ed0b8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed0b8-110">PARAMETERS</span></span>

### <span data-ttu-id="ed0b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0b8-111">-DefaultProfile</span></span>
<span data-ttu-id="ed0b8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed0b8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b8-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ed0b8-113">-IntervalInSeconds</span></span>
<span data-ttu-id="ed0b8-114">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ed0b8-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="ed0b8-115">Значение по умолчанию: 30</span><span class="sxs-lookup"><span data-stu-id="ed0b8-115">Default value is 30</span></span>

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

### <span data-ttu-id="ed0b8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed0b8-116">-Name</span></span>
<span data-ttu-id="ed0b8-117">имя параметра проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ed0b8-117">health probe setting name.</span></span>

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

### <span data-ttu-id="ed0b8-118">-Path</span><span class="sxs-lookup"><span data-stu-id="ed0b8-118">-Path</span></span>
<span data-ttu-id="ed0b8-119">Путь, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ed0b8-119">The path to use for the health probe.</span></span>
<span data-ttu-id="ed0b8-120">По умолчанию —/</span><span class="sxs-lookup"><span data-stu-id="ed0b8-120">Default is /</span></span>

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

### <span data-ttu-id="ed0b8-121">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ed0b8-121">-Protocol</span></span>
<span data-ttu-id="ed0b8-122">Схема протоколов, используемая для этого значения по умолчанию для пробной проверки — HTTP</span><span class="sxs-lookup"><span data-stu-id="ed0b8-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="ed0b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0b8-123">CommonParameters</span></span>
<span data-ttu-id="ed0b8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed0b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0b8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0b8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed0b8-126">INPUTS</span></span>

### <span data-ttu-id="ed0b8-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed0b8-127">None</span></span>

## <span data-ttu-id="ed0b8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed0b8-128">OUTPUTS</span></span>

### <span data-ttu-id="ed0b8-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="ed0b8-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="ed0b8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed0b8-130">NOTES</span></span>

## <span data-ttu-id="ed0b8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed0b8-131">RELATED LINKS</span></span>

<span data-ttu-id="ed0b8-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ed0b8-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
