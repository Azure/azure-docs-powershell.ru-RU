---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565132"
---
# <span data-ttu-id="6172c-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6172c-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="6172c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6172c-102">SYNOPSIS</span></span>
<span data-ttu-id="6172c-103">Получает первичные и дополнительные строки подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6172c-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6172c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6172c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6172c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6172c-105">DESCRIPTION</span></span>
<span data-ttu-id="6172c-106">Командлет **Get-AzureRmServiceBusNamespaceKey** возвращает первичные и дополнительные строки подключения для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6172c-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="6172c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6172c-107">EXAMPLES</span></span>

### <span data-ttu-id="6172c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6172c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="6172c-109">Основной и дополнительный строки подключения к указанному пространству имен.</span><span class="sxs-lookup"><span data-stu-id="6172c-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="6172c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6172c-110">PARAMETERS</span></span>

### <span data-ttu-id="6172c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6172c-111">-ResourceGroup</span></span>
<span data-ttu-id="6172c-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6172c-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="6172c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6172c-113">-DefaultProfile</span></span>
<span data-ttu-id="6172c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6172c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6172c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6172c-115">-Name</span></span>
<span data-ttu-id="6172c-116">Имя AuthorizationRule пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6172c-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6172c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6172c-117">-Namespace</span></span>
<span data-ttu-id="6172c-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6172c-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="6172c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6172c-119">CommonParameters</span></span>
<span data-ttu-id="6172c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6172c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6172c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6172c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6172c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6172c-122">INPUTS</span></span>

### <span data-ttu-id="6172c-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6172c-123">-ResourceGroup</span></span>
 <span data-ttu-id="6172c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6172c-124">System.String</span></span>
 

### <span data-ttu-id="6172c-125">-+ +</span><span class="sxs-lookup"><span data-stu-id="6172c-125">-NamespaceName</span></span>
 <span data-ttu-id="6172c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6172c-126">System.String</span></span>
 

### <span data-ttu-id="6172c-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="6172c-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="6172c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6172c-128">System.String</span></span>

## <span data-ttu-id="6172c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6172c-129">OUTPUTS</span></span>

### <span data-ttu-id="6172c-130">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6172c-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="6172c-131">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} PrimaryKey: {значение PrimaryKey value} SecondaryKey: {SecondaryKey значение} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6172c-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="6172c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6172c-132">NOTES</span></span>

## <span data-ttu-id="6172c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6172c-133">RELATED LINKS</span></span>

