---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902342"
---
# <span data-ttu-id="20fb4-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20fb4-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="20fb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="20fb4-103">Получает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="20fb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20fb4-104">SYNTAX</span></span>

### <span data-ttu-id="20fb4-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20fb4-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20fb4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="20fb4-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20fb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="20fb4-108">Командлет **Get-AzPrivateEndpointConnection** извлекает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="20fb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="20fb4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20fb4-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="20fb4-111">В этом примере показано, как получить подключение к частной конечной точке с именем MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="20fb4-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="20fb4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20fb4-112">PARAMETERS</span></span>

### <span data-ttu-id="20fb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fb4-113">-DefaultProfile</span></span>
<span data-ttu-id="20fb4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20fb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20fb4-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="20fb4-115">-Description</span></span>
<span data-ttu-id="20fb4-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="20fb4-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fb4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20fb4-117">-Name</span></span>
<span data-ttu-id="20fb4-118">Имя подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-118">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fb4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fb4-119">-ResourceGroupName</span></span>
<span data-ttu-id="20fb4-120">Имя группы ресурсов для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-120">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fb4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20fb4-121">-ResourceId</span></span>
<span data-ttu-id="20fb4-122">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-122">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fb4-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20fb4-123">-ServiceName</span></span>
<span data-ttu-id="20fb4-124">Имя службы частной ссылки с подключением к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="20fb4-124">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fb4-125">CommonParameters</span></span>
<span data-ttu-id="20fb4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20fb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fb4-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20fb4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fb4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20fb4-128">INPUTS</span></span>

### <span data-ttu-id="20fb4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="20fb4-129">System.String</span></span>

## <span data-ttu-id="20fb4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fb4-130">OUTPUTS</span></span>

### <span data-ttu-id="20fb4-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20fb4-131">System.Boolean</span></span>

## <span data-ttu-id="20fb4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="20fb4-132">NOTES</span></span>

## <span data-ttu-id="20fb4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20fb4-133">RELATED LINKS</span></span>

[<span data-ttu-id="20fb4-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20fb4-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
