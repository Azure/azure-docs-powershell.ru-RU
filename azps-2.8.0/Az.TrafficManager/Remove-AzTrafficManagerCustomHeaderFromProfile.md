---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: f7870cd3c6786388e34a9b243c962aa48788f91a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907614"
---
# <span data-ttu-id="1f933-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="1f933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f933-102">SYNOPSIS</span></span>
<span data-ttu-id="1f933-103">Удаляет данные настраиваемого заголовка из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="1f933-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="1f933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f933-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f933-105">DESCRIPTION</span></span>
<span data-ttu-id="1f933-106">Командлет **Remove-AzTrafficManagerCustomHeaderFromProfile** удаляет данные настраиваемого заголовка из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="1f933-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1f933-107">Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f933-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="1f933-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="1f933-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1f933-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f933-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="1f933-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f933-110">EXAMPLES</span></span>

### <span data-ttu-id="1f933-111">Пример 1: удаление настраиваемых данных заголовка из профиля</span><span class="sxs-lookup"><span data-stu-id="1f933-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1f933-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1f933-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1f933-113">Вторая команда удаляет данные настраиваемого заголовка из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f933-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1f933-114">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f933-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1f933-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f933-115">PARAMETERS</span></span>

### <span data-ttu-id="1f933-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-116">-DefaultProfile</span></span>
<span data-ttu-id="1f933-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f933-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f933-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f933-118">-Name</span></span>
<span data-ttu-id="1f933-119">Указывает имя удаляемых настраиваемых данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="1f933-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="1f933-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="1f933-121">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1f933-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1f933-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="1f933-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1f933-123">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f933-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1f933-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f933-124">-Confirm</span></span>
<span data-ttu-id="1f933-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f933-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f933-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f933-126">-WhatIf</span></span>
<span data-ttu-id="1f933-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f933-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f933-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f933-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f933-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f933-129">CommonParameters</span></span>
<span data-ttu-id="1f933-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f933-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f933-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f933-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f933-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f933-132">INPUTS</span></span>

### <span data-ttu-id="1f933-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1f933-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f933-134">OUTPUTS</span></span>

### <span data-ttu-id="1f933-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1f933-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f933-136">NOTES</span></span>

## <span data-ttu-id="1f933-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f933-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f933-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="1f933-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1f933-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f933-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
