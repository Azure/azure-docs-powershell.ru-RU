---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566126"
---
# <span data-ttu-id="54ba7-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="54ba7-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="54ba7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="54ba7-103">Создание определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="54ba7-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54ba7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54ba7-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ba7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="54ba7-106">Командлет **New-AzureRmPolicySetDefinition** создает определение политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="54ba7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="54ba7-108">Пример 1: Создание определения политики с помощью файла Set политики</span><span class="sxs-lookup"><span data-stu-id="54ba7-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="54ba7-109">Эта команда создает определение политики с именем VMPolicyDefinition, которое включает определения политик, указанные в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="54ba7-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="54ba7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="54ba7-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="54ba7-111">-ApiVersion</span></span>
<span data-ttu-id="54ba7-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54ba7-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="54ba7-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="54ba7-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ba7-114">-DefaultProfile</span></span>
<span data-ttu-id="54ba7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54ba7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54ba7-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="54ba7-116">-Description</span></span>
<span data-ttu-id="54ba7-117">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-117">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="54ba7-118">-DisplayName</span></span>
<span data-ttu-id="54ba7-119">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="54ba7-119">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="54ba7-120">-Metadata</span></span>
<span data-ttu-id="54ba7-121">Метаданные для определения Set политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-121">The metadata for policy set definition.</span></span> <span data-ttu-id="54ba7-122">Это может быть путь к имени файла, содержащему метаданные, или метаданным в виде строки.</span><span class="sxs-lookup"><span data-stu-id="54ba7-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54ba7-123">-Name</span></span>
<span data-ttu-id="54ba7-124">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-124">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-125">-Параметр</span><span class="sxs-lookup"><span data-stu-id="54ba7-125">-Parameter</span></span>
<span data-ttu-id="54ba7-126">Объявление параметров для определения задания политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="54ba7-127">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="54ba7-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="54ba7-128">-PolicyDefinition</span></span>
<span data-ttu-id="54ba7-129">Определение настройки политики.</span><span class="sxs-lookup"><span data-stu-id="54ba7-129">The policy set definition.</span></span> <span data-ttu-id="54ba7-130">Это может быть путь к имени файла, содержащему определения политики, или определению политики как String.</span><span class="sxs-lookup"><span data-stu-id="54ba7-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="54ba7-131">-Pre</span></span>
<span data-ttu-id="54ba7-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="54ba7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54ba7-133">-Confirm</span></span>
<span data-ttu-id="54ba7-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54ba7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ba7-135">-WhatIf</span></span>
<span data-ttu-id="54ba7-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54ba7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54ba7-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54ba7-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ba7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ba7-138">CommonParameters</span></span>
<span data-ttu-id="54ba7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54ba7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ba7-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ba7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ba7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54ba7-141">INPUTS</span></span>

### <span data-ttu-id="54ba7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="54ba7-142">System.String</span></span>

## <span data-ttu-id="54ba7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54ba7-143">OUTPUTS</span></span>

### <span data-ttu-id="54ba7-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="54ba7-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="54ba7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="54ba7-145">NOTES</span></span>

## <span data-ttu-id="54ba7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54ba7-146">RELATED LINKS</span></span>
