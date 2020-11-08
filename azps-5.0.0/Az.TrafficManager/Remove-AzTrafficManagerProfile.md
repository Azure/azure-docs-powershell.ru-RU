---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248440"
---
# <span data-ttu-id="074ed-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="074ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="074ed-102">SYNOPSIS</span></span>
<span data-ttu-id="074ed-103">Удаление профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="074ed-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="074ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="074ed-104">SYNTAX</span></span>

### <span data-ttu-id="074ed-105">»</span><span class="sxs-lookup"><span data-stu-id="074ed-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="074ed-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="074ed-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="074ed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="074ed-107">DESCRIPTION</span></span>
<span data-ttu-id="074ed-108">Командлет **Remove-AzTrafficManagerProfile** удаляет профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="074ed-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="074ed-109">Укажите профиль для удаления с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="074ed-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="074ed-110">Кроме того, вы можете указать объект **TrafficManagerProfile** с помощью параметра *TrafficManagerProfile* или же можно использовать конвейер.</span><span class="sxs-lookup"><span data-stu-id="074ed-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="074ed-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="074ed-111">EXAMPLES</span></span>

### <span data-ttu-id="074ed-112">Пример 1: Удаление профиля, указанного именем</span><span class="sxs-lookup"><span data-stu-id="074ed-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="074ed-113">Эта команда удаляет профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="074ed-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="074ed-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="074ed-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="074ed-115">Пример 2: Удаление профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="074ed-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="074ed-116">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="074ed-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="074ed-117">Затем команда передает этот профиль командлету **Remove-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="074ed-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="074ed-118">Этот командлет удаляет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="074ed-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="074ed-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="074ed-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="074ed-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="074ed-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="074ed-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="074ed-121">PARAMETERS</span></span>

### <span data-ttu-id="074ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-122">-DefaultProfile</span></span>
<span data-ttu-id="074ed-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="074ed-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="074ed-124">-Force</span><span class="sxs-lookup"><span data-stu-id="074ed-124">-Force</span></span>
<span data-ttu-id="074ed-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="074ed-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="074ed-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="074ed-126">-Name</span></span>
<span data-ttu-id="074ed-127">Указывает имя профиля диспетчера трафика, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="074ed-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="074ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="074ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="074ed-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="074ed-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="074ed-130">Этот командлет удаляет профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="074ed-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="074ed-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="074ed-132">Указывает объект **TrafficManagerProfile** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="074ed-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="074ed-133">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="074ed-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="074ed-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="074ed-134">-Confirm</span></span>
<span data-ttu-id="074ed-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="074ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="074ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="074ed-136">-WhatIf</span></span>
<span data-ttu-id="074ed-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="074ed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="074ed-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="074ed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="074ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074ed-139">CommonParameters</span></span>
<span data-ttu-id="074ed-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="074ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074ed-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="074ed-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074ed-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="074ed-142">INPUTS</span></span>

### <span data-ttu-id="074ed-143">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="074ed-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="074ed-144">OUTPUTS</span></span>

### <span data-ttu-id="074ed-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="074ed-145">System.Boolean</span></span>

## <span data-ttu-id="074ed-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="074ed-146">NOTES</span></span>

## <span data-ttu-id="074ed-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="074ed-147">RELATED LINKS</span></span>

[<span data-ttu-id="074ed-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="074ed-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="074ed-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="074ed-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="074ed-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="074ed-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


