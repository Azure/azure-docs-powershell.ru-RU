---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734236"
---
# <span data-ttu-id="a7f37-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7f37-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="a7f37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7f37-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f37-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7f37-104">SYNTAX</span></span>

### <span data-ttu-id="a7f37-105">Заданный параметр имени определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-105">The policy definition name parameter set.</span></span> <span data-ttu-id="a7f37-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7f37-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a7f37-107">Заданный параметр идентификатора определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a7f37-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7f37-108">DESCRIPTION</span></span>
<span data-ttu-id="a7f37-109">Командлет **Set-AzureRmPolicyDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a7f37-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7f37-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f37-111">Пример 1: Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="a7f37-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="a7f37-112">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a7f37-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a7f37-113">Команда сохраняет этот объект в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a7f37-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="a7f37-114">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a7f37-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a7f37-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7f37-115">PARAMETERS</span></span>

### <span data-ttu-id="a7f37-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a7f37-116">-ApiVersion</span></span>
<span data-ttu-id="a7f37-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7f37-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a7f37-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a7f37-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a7f37-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="a7f37-119">-Description</span></span>
<span data-ttu-id="a7f37-120">Задает новое описание для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="a7f37-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a7f37-121">-DisplayName</span></span>
<span data-ttu-id="a7f37-122">Задает новое отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="a7f37-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a7f37-123">-Id</span></span>
<span data-ttu-id="a7f37-124">Указывает полный идентификатор ресурса для определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7f37-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f37-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a7f37-125">-InformationAction</span></span>
<span data-ttu-id="a7f37-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a7f37-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a7f37-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a7f37-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7f37-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a7f37-128">Continue</span></span>
- <span data-ttu-id="a7f37-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a7f37-129">Ignore</span></span>
- <span data-ttu-id="a7f37-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a7f37-130">Inquire</span></span>
- <span data-ttu-id="a7f37-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a7f37-131">SilentlyContinue</span></span>
- <span data-ttu-id="a7f37-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="a7f37-132">Stop</span></span>
- <span data-ttu-id="a7f37-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="a7f37-133">Suspend</span></span>

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

### <span data-ttu-id="a7f37-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a7f37-134">-InformationVariable</span></span>
<span data-ttu-id="a7f37-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a7f37-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a7f37-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7f37-136">-Name</span></span>
<span data-ttu-id="a7f37-137">Указывает имя определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7f37-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f37-138">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a7f37-138">-Policy</span></span>
<span data-ttu-id="a7f37-139">Задает новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="a7f37-140">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="a7f37-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a7f37-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="a7f37-141">-Pre</span></span>
<span data-ttu-id="a7f37-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a7f37-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a7f37-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f37-143">-DefaultProfile</span></span>
<span data-ttu-id="a7f37-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f37-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f37-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a7f37-145">-Metadata</span></span>
<span data-ttu-id="a7f37-146">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-146">The metadata for policy definition.</span></span> <span data-ttu-id="a7f37-147">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a7f37-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="a7f37-148">-Параметр</span><span class="sxs-lookup"><span data-stu-id="a7f37-148">-Parameter</span></span>
<span data-ttu-id="a7f37-149">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a7f37-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a7f37-150">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявлению параметров в виде String.</span><span class="sxs-lookup"><span data-stu-id="a7f37-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a7f37-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f37-151">CommonParameters</span></span>
<span data-ttu-id="a7f37-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7f37-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f37-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f37-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f37-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7f37-154">INPUTS</span></span>

## <span data-ttu-id="a7f37-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7f37-155">OUTPUTS</span></span>

### <span data-ttu-id="a7f37-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a7f37-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a7f37-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7f37-157">NOTES</span></span>

## <span data-ttu-id="a7f37-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7f37-158">RELATED LINKS</span></span>

[<span data-ttu-id="a7f37-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7f37-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a7f37-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7f37-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a7f37-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7f37-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


