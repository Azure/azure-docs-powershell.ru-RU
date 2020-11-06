---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 81463fc5202c9b5990e5d73d81c7bc2cbeadcca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565171"
---
# <span data-ttu-id="13763-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="13763-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="13763-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13763-102">SYNOPSIS</span></span>
<span data-ttu-id="13763-103">Возвращает описание для указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="13763-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13763-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13763-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13763-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13763-105">DESCRIPTION</span></span>
<span data-ttu-id="13763-106">Командлет **Get-AzureRmWcfRelay** Возвращает описание указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="13763-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="13763-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13763-107">EXAMPLES</span></span>

### <span data-ttu-id="13763-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13763-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="13763-109">Возвращает описание WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="13763-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="13763-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13763-110">PARAMETERS</span></span>

### <span data-ttu-id="13763-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13763-111">-Namespace</span></span>
<span data-ttu-id="13763-112">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="13763-112">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13763-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13763-113">-ResourceGroupName</span></span>
<span data-ttu-id="13763-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13763-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13763-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13763-115">-Name</span></span>
<span data-ttu-id="13763-116">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="13763-116">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13763-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13763-117">-DefaultProfile</span></span>
<span data-ttu-id="13763-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13763-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13763-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13763-119">CommonParameters</span></span>
<span data-ttu-id="13763-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13763-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13763-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13763-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13763-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13763-122">INPUTS</span></span>

### <span data-ttu-id="13763-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13763-123">-ResourceGroupName</span></span>
 <span data-ttu-id="13763-124">System. String</span><span class="sxs-lookup"><span data-stu-id="13763-124">System.String</span></span>
 

### <span data-ttu-id="13763-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13763-125">-Namespace</span></span>
 <span data-ttu-id="13763-126">System. String</span><span class="sxs-lookup"><span data-stu-id="13763-126">System.String</span></span>
 

### <span data-ttu-id="13763-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13763-127">-Name</span></span>
 <span data-ttu-id="13763-128">System. String</span><span class="sxs-lookup"><span data-stu-id="13763-128">System.String</span></span> 

## <span data-ttu-id="13763-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13763-129">OUTPUTS</span></span>

### <span data-ttu-id="13763-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. WcfRelayAttributes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="13763-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="13763-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: идентификатор метаданных пользователя:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 имя: TestWCFRelay1 тип: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="13763-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="13763-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="13763-132">NOTES</span></span>

## <span data-ttu-id="13763-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13763-133">RELATED LINKS</span></span>

