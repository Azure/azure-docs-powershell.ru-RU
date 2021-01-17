---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396999"
---
# <span data-ttu-id="5cde2-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="5cde2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cde2-102">SYNOPSIS</span></span>
<span data-ttu-id="5cde2-103">Отключение профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="5cde2-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="5cde2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cde2-104">SYNTAX</span></span>

### <span data-ttu-id="5cde2-105">Поля</span><span class="sxs-lookup"><span data-stu-id="5cde2-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cde2-106">Объект</span><span class="sxs-lookup"><span data-stu-id="5cde2-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cde2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cde2-107">DESCRIPTION</span></span>
<span data-ttu-id="5cde2-108">Для отключения профиля Azure Traffic Manager будет отключен **cmdlet Disable-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="5cde2-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5cde2-109">Объект профиля можно указать с помощью конвейера или в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="5cde2-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="5cde2-110">Кроме того, можно указать профиль с помощью параметров *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="5cde2-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="5cde2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cde2-111">EXAMPLES</span></span>

### <span data-ttu-id="5cde2-112">Пример 1. Отключение профиля, указанного по имени</span><span class="sxs-lookup"><span data-stu-id="5cde2-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5cde2-113">Эта команда отключает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5cde2-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="5cde2-114">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5cde2-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="5cde2-115">Пример 2. Отключение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="5cde2-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="5cde2-116">Эта команда получает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5cde2-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="5cde2-117">Затем эта команда передает этот профиль **командлету Disable-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5cde2-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5cde2-118">Этот cmdlet отключает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="5cde2-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="5cde2-119">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="5cde2-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5cde2-120">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="5cde2-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5cde2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cde2-121">PARAMETERS</span></span>

### <span data-ttu-id="5cde2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-122">-DefaultProfile</span></span>
<span data-ttu-id="5cde2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cde2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cde2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5cde2-124">-Force</span></span>
<span data-ttu-id="5cde2-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5cde2-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5cde2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5cde2-126">-Name</span></span>
<span data-ttu-id="5cde2-127">Указывает имя профиля Диспетчера трафика, который этот cmdlet отключает.</span><span class="sxs-lookup"><span data-stu-id="5cde2-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="5cde2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cde2-128">-ResourceGroupName</span></span>
<span data-ttu-id="5cde2-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cde2-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5cde2-130">Этот cmdlet отключает профиль Диспетчера трафика в группе, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5cde2-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cde2-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="5cde2-132">Определяет объект **TrafficManagerProfile,** который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="5cde2-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="5cde2-133">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="5cde2-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="5cde2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cde2-134">-Confirm</span></span>
<span data-ttu-id="5cde2-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5cde2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cde2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cde2-136">-WhatIf</span></span>
<span data-ttu-id="5cde2-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cde2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cde2-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cde2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cde2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cde2-139">CommonParameters</span></span>
<span data-ttu-id="5cde2-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cde2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cde2-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cde2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cde2-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cde2-142">INPUTS</span></span>

### <span data-ttu-id="5cde2-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5cde2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cde2-144">OUTPUTS</span></span>

### <span data-ttu-id="5cde2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cde2-145">System.Boolean</span></span>

## <span data-ttu-id="5cde2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cde2-146">NOTES</span></span>

## <span data-ttu-id="5cde2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cde2-147">RELATED LINKS</span></span>

[<span data-ttu-id="5cde2-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="5cde2-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5cde2-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5cde2-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="5cde2-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5cde2-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


