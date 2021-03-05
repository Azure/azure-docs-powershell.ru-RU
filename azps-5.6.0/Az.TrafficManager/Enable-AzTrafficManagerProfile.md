---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: 40bfe0d68df65b7535ec40a3cb27da1501f915c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987339"
---
# <span data-ttu-id="25364-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="25364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25364-102">SYNOPSIS</span></span>
<span data-ttu-id="25364-103">Включает профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="25364-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="25364-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25364-104">SYNTAX</span></span>

### <span data-ttu-id="25364-105">Поля</span><span class="sxs-lookup"><span data-stu-id="25364-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25364-106">Объект</span><span class="sxs-lookup"><span data-stu-id="25364-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25364-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25364-107">DESCRIPTION</span></span>
<span data-ttu-id="25364-108">Для профиля Azure Traffic Manager включается **cmdlet Enable-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="25364-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="25364-109">Объект профиля можно указать с помощью конвейера или в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="25364-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="25364-110">Кроме того, можно указать профиль с помощью параметров *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="25364-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="25364-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25364-111">EXAMPLES</span></span>

### <span data-ttu-id="25364-112">Пример 1. В этом примере можно включить профиль, указанный по имени</span><span class="sxs-lookup"><span data-stu-id="25364-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="25364-113">Эта команда включает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25364-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="25364-114">Пример 2. В том, как включить профиль с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="25364-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="25364-115">Эта команда получает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25364-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="25364-116">Затем эта команда передает этот профиль **командлету Enable-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="25364-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="25364-117">Этот cmdlet включает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="25364-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="25364-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25364-118">PARAMETERS</span></span>

### <span data-ttu-id="25364-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25364-119">-DefaultProfile</span></span>
<span data-ttu-id="25364-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25364-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25364-121">-Name</span><span class="sxs-lookup"><span data-stu-id="25364-121">-Name</span></span>
<span data-ttu-id="25364-122">Указывает имя профиля Диспетчера трафика, который включает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25364-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25364-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25364-123">-ResourceGroupName</span></span>
<span data-ttu-id="25364-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25364-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="25364-125">Этот cmdlet включает профиль Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="25364-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25364-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="25364-127">Определяет объект **TrafficManagerProfile,** который нужно включить.</span><span class="sxs-lookup"><span data-stu-id="25364-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="25364-128">Чтобы получить объект **TrafficManagerProfile,** воспользуйтесь Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="25364-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25364-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25364-129">CommonParameters</span></span>
<span data-ttu-id="25364-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25364-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25364-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25364-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25364-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25364-132">INPUTS</span></span>

### <span data-ttu-id="25364-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="25364-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25364-134">OUTPUTS</span></span>

### <span data-ttu-id="25364-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25364-135">System.Boolean</span></span>

## <span data-ttu-id="25364-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25364-136">NOTES</span></span>

## <span data-ttu-id="25364-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25364-137">RELATED LINKS</span></span>

[<span data-ttu-id="25364-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="25364-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="25364-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="25364-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="25364-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25364-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


