---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561547"
---
# <span data-ttu-id="537ab-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="537ab-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="537ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="537ab-102">SYNOPSIS</span></span>
<span data-ttu-id="537ab-103">Создание определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="537ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="537ab-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="537ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="537ab-105">DESCRIPTION</span></span>
<span data-ttu-id="537ab-106">Командлет **New-AzureRmPolicyDefinition** создает определение политики, включающее правило политики в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="537ab-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="537ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="537ab-107">EXAMPLES</span></span>

### <span data-ttu-id="537ab-108">Пример 1: Создание определения политики с помощью файла политики</span><span class="sxs-lookup"><span data-stu-id="537ab-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="537ab-109">Эта команда создает определение политики с именем VMPolicyDefinition, которое включает правило политики, указанное в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="537ab-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="537ab-110">Пример 2: Создание определения политики в строке</span><span class="sxs-lookup"><span data-stu-id="537ab-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="537ab-111">Эта команда создает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="537ab-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="537ab-112">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="537ab-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="537ab-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="537ab-113">PARAMETERS</span></span>

### <span data-ttu-id="537ab-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="537ab-114">-ApiVersion</span></span>
<span data-ttu-id="537ab-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537ab-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="537ab-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="537ab-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="537ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537ab-117">-DefaultProfile</span></span>
<span data-ttu-id="537ab-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="537ab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="537ab-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="537ab-119">-Description</span></span>
<span data-ttu-id="537ab-120">Задает описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-120">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="537ab-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="537ab-121">-DisplayName</span></span>
<span data-ttu-id="537ab-122">Задает отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-122">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="537ab-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="537ab-123">-InformationAction</span></span>
<span data-ttu-id="537ab-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="537ab-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="537ab-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="537ab-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="537ab-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="537ab-126">Continue</span></span>
- <span data-ttu-id="537ab-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="537ab-127">Ignore</span></span>
- <span data-ttu-id="537ab-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="537ab-128">Inquire</span></span>
- <span data-ttu-id="537ab-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="537ab-129">SilentlyContinue</span></span>
- <span data-ttu-id="537ab-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="537ab-130">Stop</span></span>
- <span data-ttu-id="537ab-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="537ab-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537ab-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="537ab-132">-InformationVariable</span></span>
<span data-ttu-id="537ab-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="537ab-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537ab-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="537ab-134">-Metadata</span></span>
<span data-ttu-id="537ab-135">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-135">The metadata for policy definition.</span></span> <span data-ttu-id="537ab-136">Это может быть путь к имени файла, содержащему метаданные, или метаданным в виде строки.</span><span class="sxs-lookup"><span data-stu-id="537ab-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="537ab-137">Режим</span><span class="sxs-lookup"><span data-stu-id="537ab-137">-Mode</span></span>
<span data-ttu-id="537ab-138">Режим определения политики</span><span class="sxs-lookup"><span data-stu-id="537ab-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="537ab-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="537ab-139">-Name</span></span>
<span data-ttu-id="537ab-140">Задает имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-140">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="537ab-141">-Параметр</span><span class="sxs-lookup"><span data-stu-id="537ab-141">-Parameter</span></span>
<span data-ttu-id="537ab-142">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="537ab-143">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="537ab-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="537ab-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="537ab-144">-Policy</span></span>
<span data-ttu-id="537ab-145">Определяет правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="537ab-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="537ab-146">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="537ab-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="537ab-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="537ab-147">-Pre</span></span>
<span data-ttu-id="537ab-148">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="537ab-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="537ab-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537ab-149">CommonParameters</span></span>
<span data-ttu-id="537ab-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="537ab-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537ab-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="537ab-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537ab-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="537ab-152">INPUTS</span></span>

### <span data-ttu-id="537ab-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="537ab-153">None</span></span>
<span data-ttu-id="537ab-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="537ab-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="537ab-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="537ab-155">OUTPUTS</span></span>

### <span data-ttu-id="537ab-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="537ab-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="537ab-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="537ab-157">NOTES</span></span>

## <span data-ttu-id="537ab-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="537ab-158">RELATED LINKS</span></span>

[<span data-ttu-id="537ab-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="537ab-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="537ab-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="537ab-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="537ab-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="537ab-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


