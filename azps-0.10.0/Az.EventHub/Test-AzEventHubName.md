---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 49b47e637d009eabac106679e81ec763b0898160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911224"
---
# <span data-ttu-id="4b216-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="4b216-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="4b216-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b216-102">SYNOPSIS</span></span>
<span data-ttu-id="4b216-103">Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="4b216-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4b216-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b216-104">SYNTAX</span></span>

### <span data-ttu-id="4b216-105">NamespaceCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b216-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b216-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4b216-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b216-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b216-107">DESCRIPTION</span></span>
<span data-ttu-id="4b216-108">Командлет **Test-AzEventhubName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="4b216-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4b216-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b216-109">EXAMPLES</span></span>

### <span data-ttu-id="4b216-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b216-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="4b216-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина, если оно доступно</span><span class="sxs-lookup"><span data-stu-id="4b216-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="4b216-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b216-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="4b216-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины</span><span class="sxs-lookup"><span data-stu-id="4b216-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="4b216-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4b216-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="4b216-115">Возвращает состояние доступности имени псевдонима "myAliasName" для пространства имен "MyNameSapceName" как истина, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="4b216-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="4b216-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b216-116">PARAMETERS</span></span>

### <span data-ttu-id="4b216-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4b216-117">-AliasName</span></span>
<span data-ttu-id="4b216-118">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="4b216-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="4b216-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b216-119">-DefaultProfile</span></span>
<span data-ttu-id="4b216-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b216-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b216-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b216-121">-Namespace</span></span>
<span data-ttu-id="4b216-122">Имя пространства имен Eventhub</span><span class="sxs-lookup"><span data-stu-id="4b216-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="4b216-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b216-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b216-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4b216-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4b216-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b216-125">CommonParameters</span></span>
<span data-ttu-id="4b216-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b216-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b216-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b216-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b216-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b216-128">INPUTS</span></span>

### <span data-ttu-id="4b216-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b216-129">System.String</span></span>

## <span data-ttu-id="4b216-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b216-130">OUTPUTS</span></span>

### <span data-ttu-id="4b216-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="4b216-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="4b216-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b216-132">NOTES</span></span>

## <span data-ttu-id="4b216-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b216-133">RELATED LINKS</span></span>
