---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224532"
---
# <span data-ttu-id="4abb8-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="4abb8-101">Import-AzContext</span></span>

## <span data-ttu-id="4abb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4abb8-102">SYNOPSIS</span></span>
<span data-ttu-id="4abb8-103">Загружает данные проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="4abb8-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="4abb8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4abb8-104">SYNTAX</span></span>

### <span data-ttu-id="4abb8-105">ProfileFromDisk (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4abb8-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abb8-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="4abb8-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abb8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4abb8-107">DESCRIPTION</span></span>
<span data-ttu-id="4abb8-108">С Import-AzContext-файл загружает сведения проверки подлинности из файла, чтобы настроить среду и контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="4abb8-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="4abb8-109">Эти сведения используются для проверки подлинности запросов к Диспетчеру ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4abb8-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="4abb8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4abb8-110">EXAMPLES</span></span>

### <span data-ttu-id="4abb8-111">Пример 1. Импорт контекста из AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4abb8-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="4abb8-112">В этом примере импортируется контекст из PSAzureProfile, передаваемого в cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abb8-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="4abb8-113">Пример 2. Импорт контекста из файла JSON</span><span class="sxs-lookup"><span data-stu-id="4abb8-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="4abb8-114">В этом примере выбирается контекст из файла JSON, который передается в cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abb8-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="4abb8-115">Этот файл JSON можно создать из файла Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="4abb8-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="4abb8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4abb8-116">PARAMETERS</span></span>

### <span data-ttu-id="4abb8-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="4abb8-117">-AzureContext</span></span>
<span data-ttu-id="4abb8-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="4abb8-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="4abb8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abb8-119">-DefaultProfile</span></span>
<span data-ttu-id="4abb8-120">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4abb8-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4abb8-121">-Path</span><span class="sxs-lookup"><span data-stu-id="4abb8-121">-Path</span></span>
<span data-ttu-id="4abb8-122">Путь к сведениям контекста, сохраненным с помощью save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="4abb8-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="4abb8-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="4abb8-123">-Scope</span></span>
<span data-ttu-id="4abb8-124">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="4abb8-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4abb8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4abb8-125">-Confirm</span></span>
<span data-ttu-id="4abb8-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abb8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abb8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abb8-127">-WhatIf</span></span>
<span data-ttu-id="4abb8-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abb8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4abb8-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4abb8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abb8-130">CommonParameters</span></span>
<span data-ttu-id="4abb8-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abb8-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abb8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abb8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4abb8-133">INPUTS</span></span>

### <span data-ttu-id="4abb8-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4abb8-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="4abb8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4abb8-135">System.String</span></span>

## <span data-ttu-id="4abb8-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4abb8-136">OUTPUTS</span></span>

### <span data-ttu-id="4abb8-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4abb8-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="4abb8-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4abb8-138">NOTES</span></span>

## <span data-ttu-id="4abb8-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4abb8-139">RELATED LINKS</span></span>
