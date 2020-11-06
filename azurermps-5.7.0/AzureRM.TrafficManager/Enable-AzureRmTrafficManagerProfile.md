---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 252a633112c28b1dc1e62a6004e3f67e2b6a343a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566874"
---
# <span data-ttu-id="1bf16-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="1bf16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bf16-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf16-103">Включает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="1bf16-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bf16-104">SYNTAX</span></span>

### <span data-ttu-id="1bf16-105">»</span><span class="sxs-lookup"><span data-stu-id="1bf16-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf16-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="1bf16-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf16-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bf16-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf16-108">Командлет **Enable-AzureRmTrafficManagerProfile** включает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf16-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1bf16-109">Вы можете указать объект профиля с помощью конвейера или значения параметра.</span><span class="sxs-lookup"><span data-stu-id="1bf16-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="1bf16-110">Кроме того, вы можете указать профиль с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1bf16-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="1bf16-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bf16-111">EXAMPLES</span></span>

### <span data-ttu-id="1bf16-112">Пример 1: включение профиля с указанным именем</span><span class="sxs-lookup"><span data-stu-id="1bf16-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1bf16-113">Эта команда включает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1bf16-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="1bf16-114">Пример 2: включение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="1bf16-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="1bf16-115">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1bf16-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1bf16-116">Затем команда передает этот профиль командлету **Enable-AzureRmTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="1bf16-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1bf16-117">Этот командлет включает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="1bf16-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="1bf16-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bf16-118">PARAMETERS</span></span>

### <span data-ttu-id="1bf16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-119">-DefaultProfile</span></span>
<span data-ttu-id="1bf16-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf16-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf16-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1bf16-121">-Name</span></span>
<span data-ttu-id="1bf16-122">Указывает имя профиля диспетчера трафика, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1bf16-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="1bf16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf16-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bf16-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1bf16-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1bf16-125">Этот командлет включает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1bf16-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bf16-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="1bf16-127">Указывает объект **TrafficManagerProfile** для включения.</span><span class="sxs-lookup"><span data-stu-id="1bf16-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="1bf16-128">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1bf16-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1bf16-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf16-129">CommonParameters</span></span>
<span data-ttu-id="1bf16-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bf16-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf16-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf16-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf16-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bf16-132">INPUTS</span></span>

### <span data-ttu-id="1bf16-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1bf16-134">Этот командлет принимает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1bf16-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="1bf16-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bf16-135">OUTPUTS</span></span>

### <span data-ttu-id="1bf16-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bf16-136">System.Boolean</span></span>

## <span data-ttu-id="1bf16-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bf16-137">NOTES</span></span>

## <span data-ttu-id="1bf16-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bf16-138">RELATED LINKS</span></span>

[<span data-ttu-id="1bf16-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bf16-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bf16-141">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bf16-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bf16-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bf16-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


