---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077439"
---
# <span data-ttu-id="6965b-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="6965b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6965b-102">SYNOPSIS</span></span>
<span data-ttu-id="6965b-103">Получает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="6965b-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="6965b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6965b-104">SYNTAX</span></span>

### <span data-ttu-id="6965b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6965b-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6965b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6965b-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6965b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6965b-107">DESCRIPTION</span></span>
<span data-ttu-id="6965b-108">Командлет **Get-AzTrafficManagerProfile** получает профиль диспетчера трафика Azure и возвращает объект, представляющий этот профиль.</span><span class="sxs-lookup"><span data-stu-id="6965b-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="6965b-109">Укажите имя профиля и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6965b-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="6965b-110">Вы можете локально изменить этот объект, а затем применить изменения к профилю с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6965b-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="6965b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6965b-111">EXAMPLES</span></span>

### <span data-ttu-id="6965b-112">Пример 1: получение профиля</span><span class="sxs-lookup"><span data-stu-id="6965b-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="6965b-113">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6965b-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="6965b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6965b-114">PARAMETERS</span></span>

### <span data-ttu-id="6965b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-115">-DefaultProfile</span></span>
<span data-ttu-id="6965b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6965b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6965b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6965b-117">-Name</span></span>
<span data-ttu-id="6965b-118">Указывает имя профиля диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6965b-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6965b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6965b-119">-ResourceGroupName</span></span>
<span data-ttu-id="6965b-120">Указывает имя группы ресурсов, содержащей профиль диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6965b-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6965b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6965b-121">CommonParameters</span></span>
<span data-ttu-id="6965b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6965b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6965b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6965b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6965b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6965b-124">INPUTS</span></span>

### <span data-ttu-id="6965b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6965b-125">System.String</span></span>

## <span data-ttu-id="6965b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6965b-126">OUTPUTS</span></span>

### <span data-ttu-id="6965b-127">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6965b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6965b-128">NOTES</span></span>

## <span data-ttu-id="6965b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6965b-129">RELATED LINKS</span></span>

[<span data-ttu-id="6965b-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="6965b-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="6965b-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="6965b-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="6965b-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6965b-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


