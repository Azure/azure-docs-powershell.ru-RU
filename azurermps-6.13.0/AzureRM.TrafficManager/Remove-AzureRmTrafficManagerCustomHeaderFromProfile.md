---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: af18a5a93cf08fe4806af429aee667b569c527d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734582"
---
# <span data-ttu-id="2673d-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="2673d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2673d-102">SYNOPSIS</span></span>
<span data-ttu-id="2673d-103">Удаляет данные настраиваемого заголовка из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="2673d-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2673d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2673d-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromProfile -Name <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2673d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2673d-105">DESCRIPTION</span></span>
<span data-ttu-id="2673d-106">Командлет **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** удаляет данные настраиваемого заголовка из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="2673d-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2673d-107">Вы можете получить профиль, используя командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2673d-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="2673d-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="2673d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2673d-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2673d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="2673d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2673d-110">EXAMPLES</span></span>

### <span data-ttu-id="2673d-111">Пример 1: удаление настраиваемых данных заголовка из профиля</span><span class="sxs-lookup"><span data-stu-id="2673d-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2673d-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="2673d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2673d-113">Вторая команда удаляет данные настраиваемого заголовка из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2673d-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2673d-114">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2673d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2673d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2673d-115">PARAMETERS</span></span>

### <span data-ttu-id="2673d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-116">-DefaultProfile</span></span>
<span data-ttu-id="2673d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2673d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2673d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2673d-118">-Name</span></span>
<span data-ttu-id="2673d-119">Указывает имя удаляемых настраиваемых данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="2673d-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="2673d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="2673d-121">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="2673d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2673d-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="2673d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2673d-123">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2673d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2673d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2673d-124">-Confirm</span></span>
<span data-ttu-id="2673d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2673d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2673d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2673d-126">-WhatIf</span></span>
<span data-ttu-id="2673d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2673d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2673d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2673d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2673d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2673d-129">CommonParameters</span></span>
<span data-ttu-id="2673d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2673d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2673d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2673d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2673d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2673d-132">INPUTS</span></span>

### <span data-ttu-id="2673d-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2673d-134">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="2673d-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="2673d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2673d-135">OUTPUTS</span></span>

### <span data-ttu-id="2673d-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2673d-137">Этот командлет возвращает модифицированный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="2673d-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2673d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2673d-138">NOTES</span></span>

## <span data-ttu-id="2673d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2673d-139">RELATED LINKS</span></span>

[<span data-ttu-id="2673d-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="2673d-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2673d-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2673d-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
