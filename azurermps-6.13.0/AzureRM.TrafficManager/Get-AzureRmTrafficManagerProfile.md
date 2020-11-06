---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558171"
---
# <span data-ttu-id="af3d4-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="af3d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="af3d4-103">Получает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="af3d4-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af3d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af3d4-104">SYNTAX</span></span>

### <span data-ttu-id="af3d4-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="af3d4-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af3d4-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af3d4-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af3d4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3d4-107">DESCRIPTION</span></span>
<span data-ttu-id="af3d4-108">Командлет **Get-AzureRmTrafficManagerProfile** получает профиль диспетчера трафика Azure и возвращает объект, представляющий этот профиль.</span><span class="sxs-lookup"><span data-stu-id="af3d4-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="af3d4-109">Укажите имя профиля и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af3d4-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="af3d4-110">Вы можете локально изменить этот объект, а затем применить изменения к профилю с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af3d4-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="af3d4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af3d4-111">EXAMPLES</span></span>

### <span data-ttu-id="af3d4-112">Пример 1: получение профиля</span><span class="sxs-lookup"><span data-stu-id="af3d4-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="af3d4-113">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="af3d4-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="af3d4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af3d4-114">PARAMETERS</span></span>

### <span data-ttu-id="af3d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-115">-DefaultProfile</span></span>
<span data-ttu-id="af3d4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af3d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af3d4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af3d4-117">-Name</span></span>
<span data-ttu-id="af3d4-118">Указывает имя профиля диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af3d4-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af3d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="af3d4-120">Указывает имя группы ресурсов, содержащей профиль диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af3d4-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af3d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3d4-121">CommonParameters</span></span>
<span data-ttu-id="af3d4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af3d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3d4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af3d4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3d4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af3d4-124">INPUTS</span></span>

### <span data-ttu-id="af3d4-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="af3d4-125">None</span></span>
<span data-ttu-id="af3d4-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="af3d4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af3d4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3d4-127">OUTPUTS</span></span>

### <span data-ttu-id="af3d4-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="af3d4-129">Этот командлет возвращает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="af3d4-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="af3d4-130">Вы можете изменить этот объект, а затем применить изменения к диспетчеру трафика с помощью **Set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="af3d4-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="af3d4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="af3d4-131">NOTES</span></span>

## <span data-ttu-id="af3d4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af3d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="af3d4-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af3d4-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af3d4-135">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af3d4-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af3d4-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af3d4-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


