---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733202"
---
# <span data-ttu-id="f5728-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="f5728-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5728-102">SYNOPSIS</span></span>
<span data-ttu-id="f5728-103">Отключение профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f5728-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5728-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5728-104">SYNTAX</span></span>

### <span data-ttu-id="f5728-105">»</span><span class="sxs-lookup"><span data-stu-id="f5728-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5728-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="f5728-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5728-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5728-107">DESCRIPTION</span></span>
<span data-ttu-id="f5728-108">Командлет **Disable-AzureRmTrafficManagerProfile** отключает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f5728-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f5728-109">Вы можете указать объект профиля с помощью конвейера или значения параметра.</span><span class="sxs-lookup"><span data-stu-id="f5728-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="f5728-110">Кроме того, вы можете указать профиль с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f5728-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f5728-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5728-111">EXAMPLES</span></span>

### <span data-ttu-id="f5728-112">Пример 1: отключение профиля, указанного именем</span><span class="sxs-lookup"><span data-stu-id="f5728-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f5728-113">Эта команда отключает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f5728-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f5728-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f5728-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f5728-115">Пример 2: отключение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f5728-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="f5728-116">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f5728-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f5728-117">Затем команда передает этот профиль командлету **Disable-AzureRmTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5728-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5728-118">Этот командлет отключает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="f5728-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="f5728-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="f5728-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f5728-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f5728-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f5728-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5728-121">PARAMETERS</span></span>

### <span data-ttu-id="f5728-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-122">-DefaultProfile</span></span>
<span data-ttu-id="f5728-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5728-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f5728-124">-Force</span></span>
<span data-ttu-id="f5728-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5728-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5728-126">-Name</span></span>
<span data-ttu-id="f5728-127">Указывает имя профиля диспетчера трафика, который отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f5728-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5728-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5728-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5728-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f5728-130">Этот командлет отключает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f5728-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="f5728-132">Указывает объект **TrafficManagerProfile** , который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="f5728-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="f5728-133">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f5728-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5728-134">-Confirm</span></span>
<span data-ttu-id="f5728-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5728-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5728-136">-WhatIf</span></span>
<span data-ttu-id="f5728-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5728-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5728-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5728-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5728-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5728-139">CommonParameters</span></span>
<span data-ttu-id="f5728-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5728-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5728-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5728-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5728-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5728-142">INPUTS</span></span>

### <span data-ttu-id="f5728-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f5728-144">Этот командлет принимает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f5728-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f5728-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5728-145">OUTPUTS</span></span>

### <span data-ttu-id="f5728-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5728-146">System.Boolean</span></span>

## <span data-ttu-id="f5728-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5728-147">NOTES</span></span>

## <span data-ttu-id="f5728-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5728-148">RELATED LINKS</span></span>

[<span data-ttu-id="f5728-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f5728-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f5728-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f5728-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f5728-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f5728-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


