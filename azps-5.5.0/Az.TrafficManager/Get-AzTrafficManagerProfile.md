---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232316"
---
# <span data-ttu-id="c5360-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c5360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5360-102">SYNOPSIS</span></span>
<span data-ttu-id="c5360-103">Получает профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="c5360-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="c5360-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5360-104">SYNTAX</span></span>

### <span data-ttu-id="c5360-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5360-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5360-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5360-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5360-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5360-107">DESCRIPTION</span></span>
<span data-ttu-id="c5360-108">Cmdlet **Get-AzTrafficManagerProfile** получает профиль Azure Traffic Manager и возвращает объект, который представляет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="c5360-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="c5360-109">Укажите профиль по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5360-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="c5360-110">Вы можете изменить этот объект локально, а затем применить изменения к профилю с помощью Set-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="c5360-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c5360-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5360-111">EXAMPLES</span></span>

### <span data-ttu-id="c5360-112">Пример 1. Получить профиль</span><span class="sxs-lookup"><span data-stu-id="c5360-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c5360-113">Эта команда получает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c5360-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="c5360-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5360-114">PARAMETERS</span></span>

### <span data-ttu-id="c5360-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-115">-DefaultProfile</span></span>
<span data-ttu-id="c5360-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5360-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5360-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c5360-117">-Name</span></span>
<span data-ttu-id="c5360-118">Имя профиля Диспетчера трафика, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5360-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5360-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5360-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5360-120">Имя группы ресурсов, которая содержит профиль Диспетчера трафика, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5360-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5360-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5360-121">CommonParameters</span></span>
<span data-ttu-id="c5360-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5360-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5360-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5360-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5360-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5360-124">INPUTS</span></span>

### <span data-ttu-id="c5360-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c5360-125">System.String</span></span>

## <span data-ttu-id="c5360-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5360-126">OUTPUTS</span></span>

### <span data-ttu-id="c5360-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c5360-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5360-128">NOTES</span></span>

## <span data-ttu-id="c5360-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5360-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5360-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5360-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5360-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5360-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5360-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5360-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


