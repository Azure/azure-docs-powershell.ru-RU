---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556643"
---
# <span data-ttu-id="77e64-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="77e64-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="77e64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77e64-102">SYNOPSIS</span></span>
<span data-ttu-id="77e64-103">Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="77e64-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77e64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77e64-104">SYNTAX</span></span>

### <span data-ttu-id="77e64-105">NamespaceCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77e64-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e64-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="77e64-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e64-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77e64-107">DESCRIPTION</span></span>
<span data-ttu-id="77e64-108">Командлет **Test-AzureRmEventhubName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="77e64-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="77e64-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77e64-109">EXAMPLES</span></span>

### <span data-ttu-id="77e64-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77e64-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="77e64-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина, если оно доступно</span><span class="sxs-lookup"><span data-stu-id="77e64-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="77e64-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77e64-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="77e64-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины</span><span class="sxs-lookup"><span data-stu-id="77e64-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="77e64-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="77e64-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="77e64-115">Возвращает состояние доступности имени псевдонима "myAliasName" для пространства имен "MyNameSapceName" как истина, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="77e64-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="77e64-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77e64-116">PARAMETERS</span></span>

### <span data-ttu-id="77e64-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="77e64-117">-AliasName</span></span>
<span data-ttu-id="77e64-118">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="77e64-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e64-119">-DefaultProfile</span></span>
<span data-ttu-id="77e64-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77e64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e64-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77e64-121">-Namespace</span></span>
<span data-ttu-id="77e64-122">Имя пространства имен Eventhub</span><span class="sxs-lookup"><span data-stu-id="77e64-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="77e64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e64-123">-ResourceGroupName</span></span>
<span data-ttu-id="77e64-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="77e64-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e64-125">CommonParameters</span></span>
<span data-ttu-id="77e64-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77e64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e64-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e64-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e64-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77e64-128">INPUTS</span></span>

### <span data-ttu-id="77e64-129">System. String</span><span class="sxs-lookup"><span data-stu-id="77e64-129">System.String</span></span>

## <span data-ttu-id="77e64-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77e64-130">OUTPUTS</span></span>

### <span data-ttu-id="77e64-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="77e64-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="77e64-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="77e64-132">NOTES</span></span>

## <span data-ttu-id="77e64-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77e64-133">RELATED LINKS</span></span>
