---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244670"
---
# <span data-ttu-id="f56b1-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f56b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f56b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f56b1-103">Включает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f56b1-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="f56b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f56b1-104">SYNTAX</span></span>

### <span data-ttu-id="f56b1-105">»</span><span class="sxs-lookup"><span data-stu-id="f56b1-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56b1-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="f56b1-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f56b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f56b1-107">DESCRIPTION</span></span>
<span data-ttu-id="f56b1-108">Командлет **Enable-AzTrafficManagerProfile** включает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f56b1-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f56b1-109">Вы можете указать объект профиля с помощью конвейера или значения параметра.</span><span class="sxs-lookup"><span data-stu-id="f56b1-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="f56b1-110">Кроме того, вы можете указать профиль с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f56b1-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f56b1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f56b1-111">EXAMPLES</span></span>

### <span data-ttu-id="f56b1-112">Пример 1: включение профиля с указанным именем</span><span class="sxs-lookup"><span data-stu-id="f56b1-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f56b1-113">Эта команда включает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f56b1-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="f56b1-114">Пример 2: включение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f56b1-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="f56b1-115">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f56b1-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f56b1-116">Затем команда передает этот профиль командлету **Enable-AzTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f56b1-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f56b1-117">Этот командлет включает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="f56b1-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="f56b1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f56b1-118">PARAMETERS</span></span>

### <span data-ttu-id="f56b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-119">-DefaultProfile</span></span>
<span data-ttu-id="f56b1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f56b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f56b1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f56b1-121">-Name</span></span>
<span data-ttu-id="f56b1-122">Указывает имя профиля диспетчера трафика, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f56b1-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="f56b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="f56b1-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f56b1-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f56b1-125">Этот командлет включает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f56b1-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f56b1-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="f56b1-127">Указывает объект **TrafficManagerProfile** для включения.</span><span class="sxs-lookup"><span data-stu-id="f56b1-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="f56b1-128">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f56b1-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f56b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56b1-129">CommonParameters</span></span>
<span data-ttu-id="f56b1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f56b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56b1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f56b1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56b1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f56b1-132">INPUTS</span></span>

### <span data-ttu-id="f56b1-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f56b1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f56b1-134">OUTPUTS</span></span>

### <span data-ttu-id="f56b1-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f56b1-135">System.Boolean</span></span>

## <span data-ttu-id="f56b1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f56b1-136">NOTES</span></span>

## <span data-ttu-id="f56b1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f56b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="f56b1-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f56b1-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f56b1-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="f56b1-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="f56b1-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f56b1-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


