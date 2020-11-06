---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567524"
---
# <span data-ttu-id="6b4c8-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b4c8-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="6b4c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4c8-103">Создание определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b4c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b4c8-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b4c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="6b4c8-106">Командлет **New-AzureRmPolicyDefinition** создает определение политики, включающее правило политики в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="6b4c8-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="6b4c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="6b4c8-108">Пример 1: Создание определения политики с помощью файла политики</span><span class="sxs-lookup"><span data-stu-id="6b4c8-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="6b4c8-109">Эта команда создает определение политики с именем VMPolicyDefinition, которое включает правило политики, указанное в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="6b4c8-110">Пример 2: Создание определения политики в строке</span><span class="sxs-lookup"><span data-stu-id="6b4c8-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="6b4c8-111">Эта команда создает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="6b4c8-112">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="6b4c8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b4c8-113">PARAMETERS</span></span>

### <span data-ttu-id="6b4c8-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b4c8-114">-ApiVersion</span></span>
<span data-ttu-id="6b4c8-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6b4c8-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="6b4c8-117">-Description</span></span>
<span data-ttu-id="6b4c8-118">Задает описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-118">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="6b4c8-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b4c8-119">-DisplayName</span></span>
<span data-ttu-id="6b4c8-120">Задает отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-120">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="6b4c8-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b4c8-121">-InformationAction</span></span>
<span data-ttu-id="6b4c8-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b4c8-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6b4c8-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b4c8-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6b4c8-124">Continue</span></span>
- <span data-ttu-id="6b4c8-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6b4c8-125">Ignore</span></span>
- <span data-ttu-id="6b4c8-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6b4c8-126">Inquire</span></span>
- <span data-ttu-id="6b4c8-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b4c8-127">SilentlyContinue</span></span>
- <span data-ttu-id="6b4c8-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="6b4c8-128">Stop</span></span>
- <span data-ttu-id="6b4c8-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="6b4c8-129">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b4c8-130">-InformationVariable</span></span>
<span data-ttu-id="6b4c8-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-131">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b4c8-132">-Name</span></span>
<span data-ttu-id="6b4c8-133">Задает имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-134">-Параметр</span><span class="sxs-lookup"><span data-stu-id="6b4c8-134">-Parameter</span></span>
<span data-ttu-id="6b4c8-135">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="6b4c8-136">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="6b4c8-137">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="6b4c8-137">-Policy</span></span>
<span data-ttu-id="6b4c8-138">Определяет правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="6b4c8-139">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b4c8-140">-Pre</span></span>
<span data-ttu-id="6b4c8-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4c8-142">-DefaultProfile</span></span>
<span data-ttu-id="6b4c8-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b4c8-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6b4c8-144">-Metadata</span></span>
<span data-ttu-id="6b4c8-145">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-145">The metadata for policy definition.</span></span> <span data-ttu-id="6b4c8-146">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="6b4c8-147">Режим</span><span class="sxs-lookup"><span data-stu-id="6b4c8-147">-Mode</span></span>
<span data-ttu-id="6b4c8-148">Режим определения политики.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4c8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4c8-149">CommonParameters</span></span>
<span data-ttu-id="6b4c8-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b4c8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4c8-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b4c8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4c8-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b4c8-152">INPUTS</span></span>

## <span data-ttu-id="6b4c8-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b4c8-153">OUTPUTS</span></span>

### <span data-ttu-id="6b4c8-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6b4c8-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6b4c8-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b4c8-155">NOTES</span></span>

## <span data-ttu-id="6b4c8-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b4c8-156">RELATED LINKS</span></span>

[<span data-ttu-id="6b4c8-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b4c8-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6b4c8-158">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b4c8-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6b4c8-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b4c8-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


