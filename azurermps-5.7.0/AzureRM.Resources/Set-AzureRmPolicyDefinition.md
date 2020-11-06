---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567406"
---
# <span data-ttu-id="237b3-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="237b3-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="237b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="237b3-102">SYNOPSIS</span></span>
<span data-ttu-id="237b3-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="237b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="237b3-104">SYNTAX</span></span>

### <span data-ttu-id="237b3-105">SetByPolicyDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="237b3-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="237b3-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="237b3-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="237b3-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="237b3-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="237b3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="237b3-108">DESCRIPTION</span></span>
<span data-ttu-id="237b3-109">Командлет **Set-AzureRmPolicyDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="237b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="237b3-110">EXAMPLES</span></span>

### <span data-ttu-id="237b3-111">Пример 1: Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="237b3-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="237b3-112">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="237b3-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="237b3-113">Команда сохраняет этот объект в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="237b3-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="237b3-114">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="237b3-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="237b3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="237b3-115">PARAMETERS</span></span>

### <span data-ttu-id="237b3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="237b3-116">-ApiVersion</span></span>
<span data-ttu-id="237b3-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="237b3-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="237b3-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="237b3-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="237b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237b3-119">-DefaultProfile</span></span>
<span data-ttu-id="237b3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="237b3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="237b3-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="237b3-121">-Description</span></span>
<span data-ttu-id="237b3-122">Задает новое описание для определения политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-122">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="237b3-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="237b3-123">-DisplayName</span></span>
<span data-ttu-id="237b3-124">Задает новое отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-124">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="237b3-125">-ID</span><span class="sxs-lookup"><span data-stu-id="237b3-125">-Id</span></span>
<span data-ttu-id="237b3-126">Указывает полный идентификатор ресурса для определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="237b3-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237b3-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="237b3-127">-InformationAction</span></span>
<span data-ttu-id="237b3-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="237b3-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="237b3-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="237b3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="237b3-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="237b3-130">Continue</span></span>
- <span data-ttu-id="237b3-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="237b3-131">Ignore</span></span>
- <span data-ttu-id="237b3-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="237b3-132">Inquire</span></span>
- <span data-ttu-id="237b3-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="237b3-133">SilentlyContinue</span></span>
- <span data-ttu-id="237b3-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="237b3-134">Stop</span></span>
- <span data-ttu-id="237b3-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="237b3-135">Suspend</span></span>

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

### <span data-ttu-id="237b3-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="237b3-136">-InformationVariable</span></span>
<span data-ttu-id="237b3-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="237b3-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="237b3-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="237b3-138">-Metadata</span></span>
<span data-ttu-id="237b3-139">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-139">The metadata for policy definition.</span></span> <span data-ttu-id="237b3-140">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="237b3-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="237b3-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="237b3-141">-Name</span></span>
<span data-ttu-id="237b3-142">Указывает имя определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="237b3-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237b3-143">-Параметр</span><span class="sxs-lookup"><span data-stu-id="237b3-143">-Parameter</span></span>
<span data-ttu-id="237b3-144">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="237b3-145">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявлению параметров в виде String.</span><span class="sxs-lookup"><span data-stu-id="237b3-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="237b3-146">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="237b3-146">-Policy</span></span>
<span data-ttu-id="237b3-147">Задает новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="237b3-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="237b3-148">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="237b3-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="237b3-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="237b3-149">-Pre</span></span>
<span data-ttu-id="237b3-150">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="237b3-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="237b3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237b3-151">CommonParameters</span></span>
<span data-ttu-id="237b3-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="237b3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237b3-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237b3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237b3-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="237b3-154">INPUTS</span></span>

### <span data-ttu-id="237b3-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="237b3-155">None</span></span>
<span data-ttu-id="237b3-156">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="237b3-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="237b3-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="237b3-157">OUTPUTS</span></span>

### <span data-ttu-id="237b3-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="237b3-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="237b3-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="237b3-159">NOTES</span></span>

## <span data-ttu-id="237b3-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="237b3-160">RELATED LINKS</span></span>

[<span data-ttu-id="237b3-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="237b3-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="237b3-162">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="237b3-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="237b3-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="237b3-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


