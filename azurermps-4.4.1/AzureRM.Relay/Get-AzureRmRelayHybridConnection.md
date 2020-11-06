---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562231"
---
# <span data-ttu-id="1b1f0-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="1b1f0-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="1b1f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1f0-103">Возвращает описание указанного HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b1f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b1f0-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b1f0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1f0-106">Командлет **Get-AzureRmRelayHybridConnection** Возвращает описание указанной HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="1b1f0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="1b1f0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b1f0-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="1b1f0-109">Возвращает описание HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="1b1f0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b1f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1b1f0-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b1f0-111">-Name</span></span>
<span data-ttu-id="1b1f0-112">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="1b1f0-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1b1f0-113">-Namespace</span></span>
<span data-ttu-id="1b1f0-114">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-114">Namespace Name.</span></span>

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

### <span data-ttu-id="1b1f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="1b1f0-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="1b1f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1f0-117">-DefaultProfile</span></span>
<span data-ttu-id="1b1f0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b1f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1f0-119">CommonParameters</span></span>
<span data-ttu-id="1b1f0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1f0-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1f0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b1f0-122">INPUTS</span></span>

### <span data-ttu-id="1b1f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1f0-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="1b1f0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1b1f0-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="1b1f0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b1f0-125">-Name</span></span>
    System.String

## <span data-ttu-id="1b1f0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b1f0-126">OUTPUTS</span></span>

### <span data-ttu-id="1b1f0-127">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. HybridConnectionAttibutes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1b1f0-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1b1f0-128">CreatedAt: 4/12/2017 3:17:02 UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: ИД метаданных пользователя:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="1b1f0-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="1b1f0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b1f0-129">NOTES</span></span>

## <span data-ttu-id="1b1f0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b1f0-130">RELATED LINKS</span></span>

