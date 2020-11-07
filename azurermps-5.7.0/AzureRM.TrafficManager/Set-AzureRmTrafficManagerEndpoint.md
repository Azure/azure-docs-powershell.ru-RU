---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732506"
---
# <span data-ttu-id="724df-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="724df-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="724df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="724df-102">SYNOPSIS</span></span>
<span data-ttu-id="724df-103">Обновляет конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="724df-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="724df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="724df-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="724df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="724df-105">DESCRIPTION</span></span>
<span data-ttu-id="724df-106">Командлет **Set-AzureRmTrafficManagerEndpoint** обновляет конечную точку в диспетчере трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="724df-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="724df-107">Этот командлет обновляет параметры из локального объекта конечной точки.</span><span class="sxs-lookup"><span data-stu-id="724df-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="724df-108">Вы можете указать объект конечной точки либо с помощью параметра *TrafficManagerEndpoint* , либо с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="724df-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="724df-109">Вы можете получить локальный объект, который представляет конечную точку, используя командлет Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="724df-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="724df-110">Измените объект на локальном компьютере, а затем используйте **Set-AzureRmTrafficManagerEndpoint** , чтобы зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="724df-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="724df-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="724df-111">EXAMPLES</span></span>

### <span data-ttu-id="724df-112">Пример 1: обновление конечной точки</span><span class="sxs-lookup"><span data-stu-id="724df-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="724df-113">Первая команда получает конечную точку диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="724df-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="724df-114">Команда хранит конечную точку локально в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="724df-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="724df-115">Вторая команда изменяет локальную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="724df-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="724df-116">Эта команда изменяет значение веса конечной точки на 20.</span><span class="sxs-lookup"><span data-stu-id="724df-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="724df-117">Третья команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="724df-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="724df-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="724df-118">PARAMETERS</span></span>

### <span data-ttu-id="724df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724df-119">-DefaultProfile</span></span>
<span data-ttu-id="724df-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="724df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="724df-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="724df-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="724df-122">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="724df-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="724df-123">Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.</span><span class="sxs-lookup"><span data-stu-id="724df-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="724df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724df-124">CommonParameters</span></span>
<span data-ttu-id="724df-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="724df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724df-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724df-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="724df-127">INPUTS</span></span>

### <span data-ttu-id="724df-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="724df-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="724df-129">Этот командлет принимает объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="724df-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="724df-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="724df-130">OUTPUTS</span></span>

### <span data-ttu-id="724df-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="724df-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="724df-132">Этот командлет возвращает объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="724df-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="724df-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="724df-133">NOTES</span></span>

## <span data-ttu-id="724df-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="724df-134">RELATED LINKS</span></span>

