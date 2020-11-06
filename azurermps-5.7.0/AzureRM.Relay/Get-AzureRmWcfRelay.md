---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567954"
---
# <span data-ttu-id="07a7d-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="07a7d-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="07a7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="07a7d-103">Возвращает описание для указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="07a7d-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07a7d-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07a7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="07a7d-106">Командлет **Get-AzureRmWcfRelay** Возвращает описание указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="07a7d-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="07a7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="07a7d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07a7d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="07a7d-109">Возвращает описание WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="07a7d-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="07a7d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="07a7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a7d-111">-DefaultProfile</span></span>
<span data-ttu-id="07a7d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07a7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07a7d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07a7d-113">-Name</span></span>
<span data-ttu-id="07a7d-114">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="07a7d-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07a7d-115">-Namespace</span></span>
<span data-ttu-id="07a7d-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="07a7d-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="07a7d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07a7d-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a7d-119">CommonParameters</span></span>
<span data-ttu-id="07a7d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07a7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a7d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a7d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a7d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07a7d-122">INPUTS</span></span>

### <span data-ttu-id="07a7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a7d-123">-ResourceGroupName</span></span>
 <span data-ttu-id="07a7d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="07a7d-124">System.String</span></span>
 

### <span data-ttu-id="07a7d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07a7d-125">-Namespace</span></span>
 <span data-ttu-id="07a7d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="07a7d-126">System.String</span></span>
 

### <span data-ttu-id="07a7d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07a7d-127">-Name</span></span>
 <span data-ttu-id="07a7d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="07a7d-128">System.String</span></span> 

## <span data-ttu-id="07a7d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a7d-129">OUTPUTS</span></span>

### <span data-ttu-id="07a7d-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. WcfRelayAttributes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="07a7d-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="07a7d-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: идентификатор метаданных пользователя:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 имя: TestWCFRelay1 тип: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="07a7d-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="07a7d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="07a7d-132">NOTES</span></span>

## <span data-ttu-id="07a7d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07a7d-133">RELATED LINKS</span></span>

