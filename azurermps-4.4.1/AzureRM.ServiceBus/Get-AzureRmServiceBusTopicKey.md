---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568305"
---
# <span data-ttu-id="9e8e5-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="9e8e5-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="9e8e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e8e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8e5-103">Получает первичные и дополнительные строки подключения для раздела служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e8e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e8e5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e8e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e8e5-105">DESCRIPTION</span></span>
<span data-ttu-id="9e8e5-106">Командлет **Get-AzureRmServiceBusTopicKey** Возвращает основную и вспомогательную строки подключения для заданной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="9e8e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e8e5-107">EXAMPLES</span></span>

### <span data-ttu-id="9e8e5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e8e5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="9e8e5-109">Возвращает основную и вспомогательную строки подключения для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="9e8e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e8e5-110">PARAMETERS</span></span>

### <span data-ttu-id="9e8e5-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e5-111">-ResourceGroup</span></span>
<span data-ttu-id="9e8e5-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e8e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e8e5-113">-DefaultProfile</span></span>
<span data-ttu-id="9e8e5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e8e5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e8e5-115">-Name</span></span>
<span data-ttu-id="9e8e5-116">Название темы AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e5-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e8e5-117">-Namespace</span></span>
<span data-ttu-id="9e8e5-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e5-119">-Темы</span><span class="sxs-lookup"><span data-stu-id="9e8e5-119">-Topic</span></span>
<span data-ttu-id="9e8e5-120">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8e5-121">CommonParameters</span></span>
<span data-ttu-id="9e8e5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8e5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e8e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8e5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e8e5-124">INPUTS</span></span>

### <span data-ttu-id="9e8e5-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e5-125">-ResourceGroup</span></span>
 <span data-ttu-id="9e8e5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9e8e5-126">System.String</span></span>
 

### <span data-ttu-id="9e8e5-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="9e8e5-127">-NamespaceName</span></span>
 <span data-ttu-id="9e8e5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e8e5-128">System.String</span></span>
 

### <span data-ttu-id="9e8e5-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="9e8e5-129">-TopicName</span></span>
 <span data-ttu-id="9e8e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9e8e5-130">System.String</span></span>
 

### <span data-ttu-id="9e8e5-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9e8e5-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9e8e5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9e8e5-132">System.String</span></span>

## <span data-ttu-id="9e8e5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e8e5-133">OUTPUTS</span></span>

### <span data-ttu-id="9e8e5-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9e8e5-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="9e8e5-135">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-to pic_exampl1 PrimaryKey: {value PrimaryKey} SecondaryKey: {SecondaryKey value} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="9e8e5-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="9e8e5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e8e5-136">NOTES</span></span>

## <span data-ttu-id="9e8e5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e8e5-137">RELATED LINKS</span></span>

