---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419815"
---
# <span data-ttu-id="be42f-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="be42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be42f-102">SYNOPSIS</span></span>
<span data-ttu-id="be42f-103">Удаляет профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="be42f-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="be42f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be42f-104">SYNTAX</span></span>

### <span data-ttu-id="be42f-105">Поля</span><span class="sxs-lookup"><span data-stu-id="be42f-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be42f-106">Объект</span><span class="sxs-lookup"><span data-stu-id="be42f-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be42f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be42f-107">DESCRIPTION</span></span>
<span data-ttu-id="be42f-108">Для удаления профиля Диспетчера трафика Azure удаляется **cmdlet Remove-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="be42f-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="be42f-109">Укажите профиль, который нужно удалить, с помощью параметров *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="be42f-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="be42f-110">Кроме того, вы можете указать объект **TrafficManagerProfile** с помощью параметра *TrafficManagerProfile* или использовать конвейер.</span><span class="sxs-lookup"><span data-stu-id="be42f-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="be42f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be42f-111">EXAMPLES</span></span>

### <span data-ttu-id="be42f-112">Пример 1. Удаление профиля, указанного по имени</span><span class="sxs-lookup"><span data-stu-id="be42f-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="be42f-113">Эта команда удаляет профиль ContosoProfile из ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="be42f-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="be42f-114">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="be42f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="be42f-115">Пример 2. Удаление профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="be42f-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="be42f-116">Эта команда получает профиль ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="be42f-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="be42f-117">Затем эта команда передает этот профиль **командлету Remove-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="be42f-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="be42f-118">Этот cmdlet удаляет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="be42f-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="be42f-119">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="be42f-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="be42f-120">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="be42f-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="be42f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be42f-121">PARAMETERS</span></span>

### <span data-ttu-id="be42f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-122">-DefaultProfile</span></span>
<span data-ttu-id="be42f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be42f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be42f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="be42f-124">-Force</span></span>
<span data-ttu-id="be42f-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="be42f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be42f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="be42f-126">-Name</span></span>
<span data-ttu-id="be42f-127">Имя профиля Диспетчера трафика, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be42f-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="be42f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be42f-128">-ResourceGroupName</span></span>
<span data-ttu-id="be42f-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be42f-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="be42f-130">Этот cmdlet удаляет профиль Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="be42f-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="be42f-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="be42f-132">Определяет объект **TrafficManagerProfile,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="be42f-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="be42f-133">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="be42f-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="be42f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be42f-134">-Confirm</span></span>
<span data-ttu-id="be42f-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="be42f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be42f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be42f-136">-WhatIf</span></span>
<span data-ttu-id="be42f-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be42f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be42f-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be42f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be42f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be42f-139">CommonParameters</span></span>
<span data-ttu-id="be42f-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be42f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be42f-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be42f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be42f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be42f-142">INPUTS</span></span>

### <span data-ttu-id="be42f-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="be42f-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be42f-144">OUTPUTS</span></span>

### <span data-ttu-id="be42f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be42f-145">System.Boolean</span></span>

## <span data-ttu-id="be42f-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be42f-146">NOTES</span></span>

## <span data-ttu-id="be42f-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be42f-147">RELATED LINKS</span></span>

[<span data-ttu-id="be42f-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="be42f-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="be42f-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="be42f-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="be42f-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be42f-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


