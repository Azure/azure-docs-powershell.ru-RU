---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 6be04cea9e3e73a06cdbb1ee449adaefd4fe803e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734750"
---
# <span data-ttu-id="a1943-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="a1943-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1943-102">SYNOPSIS</span></span>
<span data-ttu-id="a1943-103">Получает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="a1943-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1943-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1943-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1943-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1943-105">DESCRIPTION</span></span>
<span data-ttu-id="a1943-106">Командлет **Get-AzureRmTrafficManagerProfile** получает профиль диспетчера трафика Azure и возвращает объект, представляющий этот профиль.</span><span class="sxs-lookup"><span data-stu-id="a1943-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="a1943-107">Укажите имя профиля и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1943-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="a1943-108">Вы можете локально изменить этот объект, а затем применить изменения к профилю с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a1943-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a1943-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1943-109">EXAMPLES</span></span>

### <span data-ttu-id="a1943-110">Пример 1: получение профиля</span><span class="sxs-lookup"><span data-stu-id="a1943-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a1943-111">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a1943-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="a1943-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1943-112">PARAMETERS</span></span>

### <span data-ttu-id="a1943-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1943-113">-Name</span></span>
<span data-ttu-id="a1943-114">Указывает имя профиля диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1943-114">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1943-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1943-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1943-116">Указывает имя группы ресурсов, содержащей профиль диспетчера трафика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1943-116">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1943-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-117">-DefaultProfile</span></span>
<span data-ttu-id="a1943-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1943-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1943-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1943-119">CommonParameters</span></span>
<span data-ttu-id="a1943-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1943-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1943-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1943-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1943-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1943-122">INPUTS</span></span>

## <span data-ttu-id="a1943-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1943-123">OUTPUTS</span></span>

### <span data-ttu-id="a1943-124">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-124">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a1943-125">Этот командлет возвращает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="a1943-125">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a1943-126">Вы можете изменить этот объект, а затем применить изменения к диспетчеру трафика с помощью **Set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="a1943-126">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="a1943-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1943-127">NOTES</span></span>

## <span data-ttu-id="a1943-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1943-128">RELATED LINKS</span></span>

[<span data-ttu-id="a1943-129">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-129">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a1943-130">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-130">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a1943-131">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-131">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a1943-132">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-132">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a1943-133">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a1943-133">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


