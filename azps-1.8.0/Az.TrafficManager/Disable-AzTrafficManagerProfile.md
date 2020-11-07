---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: e0702c8893aad7f82de5de5681d8cc14da0b3681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728408"
---
# <span data-ttu-id="61f69-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="61f69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61f69-102">SYNOPSIS</span></span>
<span data-ttu-id="61f69-103">Отключение профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="61f69-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="61f69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61f69-104">SYNTAX</span></span>

### <span data-ttu-id="61f69-105">»</span><span class="sxs-lookup"><span data-stu-id="61f69-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f69-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="61f69-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f69-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f69-107">DESCRIPTION</span></span>
<span data-ttu-id="61f69-108">Командлет **Disable-AzTrafficManagerProfile** отключает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="61f69-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="61f69-109">Вы можете указать объект профиля с помощью конвейера или значения параметра.</span><span class="sxs-lookup"><span data-stu-id="61f69-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="61f69-110">Кроме того, вы можете указать профиль с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="61f69-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="61f69-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61f69-111">EXAMPLES</span></span>

### <span data-ttu-id="61f69-112">Пример 1: отключение профиля, указанного именем</span><span class="sxs-lookup"><span data-stu-id="61f69-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="61f69-113">Эта команда отключает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="61f69-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="61f69-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="61f69-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="61f69-115">Пример 2: отключение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="61f69-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="61f69-116">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="61f69-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="61f69-117">Затем команда передает этот профиль командлету **Disable-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="61f69-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61f69-118">Этот командлет отключает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="61f69-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="61f69-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="61f69-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="61f69-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="61f69-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="61f69-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61f69-121">PARAMETERS</span></span>

### <span data-ttu-id="61f69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-122">-DefaultProfile</span></span>
<span data-ttu-id="61f69-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61f69-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f69-124">-Force</span><span class="sxs-lookup"><span data-stu-id="61f69-124">-Force</span></span>
<span data-ttu-id="61f69-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="61f69-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61f69-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61f69-126">-Name</span></span>
<span data-ttu-id="61f69-127">Указывает имя профиля диспетчера трафика, который отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="61f69-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="61f69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f69-128">-ResourceGroupName</span></span>
<span data-ttu-id="61f69-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61f69-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="61f69-130">Этот командлет отключает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="61f69-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="61f69-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="61f69-132">Указывает объект **TrafficManagerProfile** , который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="61f69-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="61f69-133">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="61f69-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="61f69-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61f69-134">-Confirm</span></span>
<span data-ttu-id="61f69-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61f69-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f69-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f69-136">-WhatIf</span></span>
<span data-ttu-id="61f69-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61f69-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f69-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61f69-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f69-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f69-139">CommonParameters</span></span>
<span data-ttu-id="61f69-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61f69-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f69-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f69-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f69-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61f69-142">INPUTS</span></span>

### <span data-ttu-id="61f69-143">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="61f69-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f69-144">OUTPUTS</span></span>

### <span data-ttu-id="61f69-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61f69-145">System.Boolean</span></span>

## <span data-ttu-id="61f69-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="61f69-146">NOTES</span></span>

## <span data-ttu-id="61f69-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61f69-147">RELATED LINKS</span></span>

[<span data-ttu-id="61f69-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="61f69-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="61f69-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="61f69-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="61f69-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="61f69-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


