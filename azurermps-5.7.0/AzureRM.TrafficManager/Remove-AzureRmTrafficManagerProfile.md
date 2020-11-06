---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563224"
---
# <span data-ttu-id="2c2ad-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="2c2ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2ad-103">Удаление профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c2ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c2ad-104">SYNTAX</span></span>

### <span data-ttu-id="2c2ad-105">»</span><span class="sxs-lookup"><span data-stu-id="2c2ad-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c2ad-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="2c2ad-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c2ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c2ad-107">DESCRIPTION</span></span>
<span data-ttu-id="2c2ad-108">Командлет **Remove-AzureRmTrafficManagerProfile** удаляет профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2c2ad-109">Укажите профиль для удаления с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2c2ad-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2c2ad-110">Кроме того, вы можете указать объект **TrafficManagerProfile** с помощью параметра *TrafficManagerProfile* или же можно использовать конвейер.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="2c2ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c2ad-111">EXAMPLES</span></span>

### <span data-ttu-id="2c2ad-112">Пример 1: Удаление профиля, указанного именем</span><span class="sxs-lookup"><span data-stu-id="2c2ad-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2c2ad-113">Эта команда удаляет профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2c2ad-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="2c2ad-115">Пример 2: Удаление профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="2c2ad-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="2c2ad-116">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2c2ad-117">Затем команда передает этот профиль командлету **Remove-AzureRmTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2c2ad-118">Этот командлет удаляет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="2c2ad-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="2c2ad-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2c2ad-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2c2ad-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c2ad-121">PARAMETERS</span></span>

### <span data-ttu-id="2c2ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-122">-DefaultProfile</span></span>
<span data-ttu-id="2c2ad-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2ad-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2c2ad-124">-Force</span></span>
<span data-ttu-id="2c2ad-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c2ad-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c2ad-126">-Name</span></span>
<span data-ttu-id="2c2ad-127">Указывает имя профиля диспетчера трафика, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2c2ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c2ad-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2c2ad-130">Этот командлет удаляет профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c2ad-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="2c2ad-132">Указывает объект **TrafficManagerProfile** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="2c2ad-133">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2c2ad-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c2ad-134">-Confirm</span></span>
<span data-ttu-id="2c2ad-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c2ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c2ad-136">-WhatIf</span></span>
<span data-ttu-id="2c2ad-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c2ad-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c2ad-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2ad-139">CommonParameters</span></span>
<span data-ttu-id="2c2ad-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2ad-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c2ad-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2ad-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c2ad-142">INPUTS</span></span>

### <span data-ttu-id="2c2ad-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2c2ad-144">Этот командлет принимает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="2c2ad-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2c2ad-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c2ad-145">OUTPUTS</span></span>

### <span data-ttu-id="2c2ad-146">Значением</span><span class="sxs-lookup"><span data-stu-id="2c2ad-146">Boolean</span></span>
<span data-ttu-id="2c2ad-147">Этот командлет возвращает значение $True, если оно прошло успешно, или, если при удалении происходит сбой, значение $False.</span><span class="sxs-lookup"><span data-stu-id="2c2ad-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="2c2ad-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c2ad-148">NOTES</span></span>

## <span data-ttu-id="2c2ad-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c2ad-149">RELATED LINKS</span></span>

[<span data-ttu-id="2c2ad-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2c2ad-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2c2ad-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2c2ad-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2c2ad-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ad-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


