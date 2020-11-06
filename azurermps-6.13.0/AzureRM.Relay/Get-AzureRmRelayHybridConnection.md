---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 468128f16c3a5ef7ef4b400694dbcc1c570f5488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569748"
---
# <span data-ttu-id="98290-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="98290-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="98290-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98290-102">SYNOPSIS</span></span>
<span data-ttu-id="98290-103">Возвращает описание указанного HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="98290-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98290-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98290-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98290-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98290-105">DESCRIPTION</span></span>
<span data-ttu-id="98290-106">Командлет **Get-AzureRmRelayHybridConnection** Возвращает описание указанной HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="98290-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="98290-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98290-107">EXAMPLES</span></span>

### <span data-ttu-id="98290-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98290-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="98290-109">Возвращает описание HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="98290-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="98290-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98290-110">PARAMETERS</span></span>

### <span data-ttu-id="98290-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98290-111">-DefaultProfile</span></span>
<span data-ttu-id="98290-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98290-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98290-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98290-113">-Name</span></span>
<span data-ttu-id="98290-114">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="98290-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="98290-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98290-115">-Namespace</span></span>
<span data-ttu-id="98290-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="98290-116">Namespace Name.</span></span>

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

### <span data-ttu-id="98290-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98290-117">-ResourceGroupName</span></span>
<span data-ttu-id="98290-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98290-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="98290-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98290-119">CommonParameters</span></span>
<span data-ttu-id="98290-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98290-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98290-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98290-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98290-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98290-122">INPUTS</span></span>

### <span data-ttu-id="98290-123">System. String</span><span class="sxs-lookup"><span data-stu-id="98290-123">System.String</span></span>


## <span data-ttu-id="98290-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98290-124">OUTPUTS</span></span>

### <span data-ttu-id="98290-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="98290-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="98290-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="98290-126">NOTES</span></span>

## <span data-ttu-id="98290-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98290-127">RELATED LINKS</span></span>
