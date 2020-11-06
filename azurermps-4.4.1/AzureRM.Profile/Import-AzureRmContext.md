---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565182"
---
# <span data-ttu-id="391ee-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="391ee-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="391ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="391ee-102">SYNOPSIS</span></span>
<span data-ttu-id="391ee-103">Загрузка данных проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="391ee-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="391ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="391ee-104">SYNTAX</span></span>

### <span data-ttu-id="391ee-105">ProfileFromDisk (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="391ee-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="391ee-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="391ee-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="391ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="391ee-107">DESCRIPTION</span></span>
<span data-ttu-id="391ee-108">Командлет Import-AzureRmContext загружает данные для проверки подлинности из файла, чтобы установить среду и контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="391ee-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="391ee-109">Командлеты, выполняемые в текущем сеансе, используют эти сведения для проверки подлинности запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="391ee-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="391ee-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="391ee-110">EXAMPLES</span></span>

### <span data-ttu-id="391ee-111">Пример 1: импорт контекста из AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="391ee-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="391ee-112">В этом примере выполняется импорт контекста из PSAzureProfile, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="391ee-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="391ee-113">Пример 2: импорт контекста из JSON-файла</span><span class="sxs-lookup"><span data-stu-id="391ee-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="391ee-114">В этом примере выделяется контекст из JSON-файла, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="391ee-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="391ee-115">Этот JSON-файл можно создать из сохраняемого AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="391ee-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="391ee-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="391ee-116">PARAMETERS</span></span>

### <span data-ttu-id="391ee-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="391ee-117">-AzureContext</span></span>
<span data-ttu-id="391ee-118">Указывает контекст Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="391ee-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="391ee-119">Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="391ee-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391ee-120">-DefaultProfile</span></span>
<span data-ttu-id="391ee-121">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="391ee-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="391ee-122">-Path</span><span class="sxs-lookup"><span data-stu-id="391ee-122">-Path</span></span>
<span data-ttu-id="391ee-123">Указывает путь к контекстной информации, сохраненной с помощью команды Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="391ee-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391ee-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="391ee-124">-Scope</span></span>
<span data-ttu-id="391ee-125">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="391ee-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391ee-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="391ee-126">-Confirm</span></span>
<span data-ttu-id="391ee-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="391ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="391ee-128">-WhatIf</span></span>
<span data-ttu-id="391ee-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="391ee-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="391ee-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="391ee-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391ee-131">CommonParameters</span></span>
<span data-ttu-id="391ee-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="391ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391ee-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="391ee-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391ee-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="391ee-134">INPUTS</span></span>

### <span data-ttu-id="391ee-135">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="391ee-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="391ee-136">Содержат набор учетных данных, учетных записей и подписок, которые используются для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="391ee-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="391ee-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="391ee-137">OUTPUTS</span></span>

### <span data-ttu-id="391ee-138">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="391ee-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="391ee-139">Содержат набор учетных данных, учетных записей и подписок, которые можно использовать для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="391ee-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="391ee-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="391ee-140">NOTES</span></span>

## <span data-ttu-id="391ee-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="391ee-141">RELATED LINKS</span></span>

