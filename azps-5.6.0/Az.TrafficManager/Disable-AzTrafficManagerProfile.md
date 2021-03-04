---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: 4d667b1435a7396082f0626d8f55882f7c37b8ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950808"
---
# <span data-ttu-id="d0877-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="d0877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0877-102">SYNOPSIS</span></span>
<span data-ttu-id="d0877-103">Отключение профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="d0877-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="d0877-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0877-104">SYNTAX</span></span>

### <span data-ttu-id="d0877-105">Поля</span><span class="sxs-lookup"><span data-stu-id="d0877-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0877-106">Объект</span><span class="sxs-lookup"><span data-stu-id="d0877-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0877-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0877-107">DESCRIPTION</span></span>
<span data-ttu-id="d0877-108">**Cmdlet Disable-AzTrafficManagerProfile** отключает профиль Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d0877-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d0877-109">Объект профиля можно указать с помощью конвейера или в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="d0877-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="d0877-110">Кроме того, можно указать профиль с помощью параметров *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="d0877-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d0877-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0877-111">EXAMPLES</span></span>

### <span data-ttu-id="d0877-112">Пример 1. Отключение профиля, указанного по имени</span><span class="sxs-lookup"><span data-stu-id="d0877-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d0877-113">Эта команда отключает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d0877-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d0877-114">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d0877-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="d0877-115">Пример 2. Отключение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="d0877-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="d0877-116">Эта команда получает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d0877-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d0877-117">Затем эта команда передает этот профиль **командлету Disable-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d0877-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d0877-118">Этот cmdlet отключает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="d0877-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="d0877-119">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="d0877-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d0877-120">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="d0877-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d0877-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0877-121">PARAMETERS</span></span>

### <span data-ttu-id="d0877-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-122">-DefaultProfile</span></span>
<span data-ttu-id="d0877-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0877-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0877-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d0877-124">-Force</span></span>
<span data-ttu-id="d0877-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d0877-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0877-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d0877-126">-Name</span></span>
<span data-ttu-id="d0877-127">Указывает имя профиля Диспетчера трафика, который этот cmdlet отключает.</span><span class="sxs-lookup"><span data-stu-id="d0877-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="d0877-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0877-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0877-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0877-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d0877-130">Этот cmdlet отключает профиль Диспетчера трафика в группе, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d0877-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0877-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="d0877-132">Определяет объект **TrafficManagerProfile,** который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="d0877-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="d0877-133">Чтобы получить объект **TrafficManagerProfile,** воспользуйтесь Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="d0877-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d0877-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0877-134">-Confirm</span></span>
<span data-ttu-id="d0877-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d0877-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0877-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0877-136">-WhatIf</span></span>
<span data-ttu-id="d0877-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0877-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0877-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d0877-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0877-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0877-139">CommonParameters</span></span>
<span data-ttu-id="d0877-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0877-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0877-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0877-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0877-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0877-142">INPUTS</span></span>

### <span data-ttu-id="d0877-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d0877-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0877-144">OUTPUTS</span></span>

### <span data-ttu-id="d0877-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0877-145">System.Boolean</span></span>

## <span data-ttu-id="d0877-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0877-146">NOTES</span></span>

## <span data-ttu-id="d0877-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0877-147">RELATED LINKS</span></span>

[<span data-ttu-id="d0877-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="d0877-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d0877-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="d0877-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="d0877-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0877-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


