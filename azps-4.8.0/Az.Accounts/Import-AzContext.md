---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245116"
---
# <span data-ttu-id="aecc9-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="aecc9-101">Import-AzContext</span></span>

## <span data-ttu-id="aecc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aecc9-102">SYNOPSIS</span></span>
<span data-ttu-id="aecc9-103">Загрузка данных проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="aecc9-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="aecc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aecc9-104">SYNTAX</span></span>

### <span data-ttu-id="aecc9-105">ProfileFromDisk (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aecc9-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aecc9-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="aecc9-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aecc9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aecc9-107">DESCRIPTION</span></span>
<span data-ttu-id="aecc9-108">Командлет Import-AzContext загружает данные для проверки подлинности из файла, чтобы установить среду и контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="aecc9-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="aecc9-109">Командлеты, выполняемые в текущем сеансе, используют эти сведения для проверки подлинности запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="aecc9-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="aecc9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aecc9-110">EXAMPLES</span></span>

### <span data-ttu-id="aecc9-111">Пример 1: импорт контекста из AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="aecc9-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="aecc9-112">В этом примере выполняется импорт контекста из PSAzureProfile, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="aecc9-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="aecc9-113">Пример 2: импорт контекста из JSON-файла</span><span class="sxs-lookup"><span data-stu-id="aecc9-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="aecc9-114">В этом примере выделяется контекст из JSON-файла, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="aecc9-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="aecc9-115">Этот JSON-файл можно создать из сохраняемого AzContext.</span><span class="sxs-lookup"><span data-stu-id="aecc9-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="aecc9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aecc9-116">PARAMETERS</span></span>

### <span data-ttu-id="aecc9-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="aecc9-117">-AzureContext</span></span>
<span data-ttu-id="aecc9-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="aecc9-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="aecc9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecc9-119">-DefaultProfile</span></span>
<span data-ttu-id="aecc9-120">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aecc9-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aecc9-121">-Path</span><span class="sxs-lookup"><span data-stu-id="aecc9-121">-Path</span></span>
<span data-ttu-id="aecc9-122">Указывает путь к контекстной информации, сохраненной с помощью команды Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="aecc9-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="aecc9-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="aecc9-123">-Scope</span></span>
<span data-ttu-id="aecc9-124">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="aecc9-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="aecc9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aecc9-125">-Confirm</span></span>
<span data-ttu-id="aecc9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aecc9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aecc9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aecc9-127">-WhatIf</span></span>
<span data-ttu-id="aecc9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aecc9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aecc9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aecc9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aecc9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecc9-130">CommonParameters</span></span>
<span data-ttu-id="aecc9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aecc9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecc9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecc9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecc9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aecc9-133">INPUTS</span></span>

### <span data-ttu-id="aecc9-134">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="aecc9-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="aecc9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="aecc9-135">System.String</span></span>

## <span data-ttu-id="aecc9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aecc9-136">OUTPUTS</span></span>

### <span data-ttu-id="aecc9-137">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="aecc9-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="aecc9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aecc9-138">NOTES</span></span>

## <span data-ttu-id="aecc9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aecc9-139">RELATED LINKS</span></span>