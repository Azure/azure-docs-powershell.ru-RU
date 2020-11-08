---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246378"
---
# <span data-ttu-id="ea7e6-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="ea7e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7e6-103">Удаляет данные настраиваемого заголовка из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ea7e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea7e6-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7e6-106">Командлет **Remove-AzTrafficManagerCustomHeaderFromProfile** удаляет данные настраиваемого заголовка из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ea7e6-107">Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ea7e6-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ea7e6-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ea7e6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea7e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7e6-111">Пример 1: удаление настраиваемых данных заголовка из профиля</span><span class="sxs-lookup"><span data-stu-id="ea7e6-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ea7e6-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="ea7e6-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ea7e6-113">Вторая команда удаляет данные настраиваемого заголовка из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ea7e6-114">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ea7e6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea7e6-115">PARAMETERS</span></span>

### <span data-ttu-id="ea7e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-116">-DefaultProfile</span></span>
<span data-ttu-id="ea7e6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7e6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea7e6-118">-Name</span></span>
<span data-ttu-id="ea7e6-119">Указывает имя удаляемых настраиваемых данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="ea7e6-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="ea7e6-121">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="ea7e6-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ea7e6-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ea7e6-123">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7e6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7e6-124">-Confirm</span></span>
<span data-ttu-id="ea7e6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7e6-126">-WhatIf</span></span>
<span data-ttu-id="ea7e6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea7e6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7e6-129">CommonParameters</span></span>
<span data-ttu-id="ea7e6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea7e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7e6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7e6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7e6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea7e6-132">INPUTS</span></span>

### <span data-ttu-id="ea7e6-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ea7e6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7e6-134">OUTPUTS</span></span>

### <span data-ttu-id="ea7e6-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ea7e6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea7e6-136">NOTES</span></span>

## <span data-ttu-id="ea7e6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea7e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="ea7e6-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="ea7e6-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ea7e6-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea7e6-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
