---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: feddd9645b22c554d5e78813194ecc8837fdf3fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910824"
---
# <span data-ttu-id="a03e2-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a03e2-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="a03e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a03e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a03e2-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="a03e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a03e2-104">SYNTAX</span></span>

### <span data-ttu-id="a03e2-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a03e2-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a03e2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03e2-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a03e2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03e2-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a03e2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03e2-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a03e2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a03e2-109">DESCRIPTION</span></span>
<span data-ttu-id="a03e2-110">Командлет **Set-AzPolicyDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a03e2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a03e2-111">EXAMPLES</span></span>

### <span data-ttu-id="a03e2-112">Пример 1: Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="a03e2-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="a03e2-113">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a03e2-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a03e2-114">Команда сохраняет этот объект в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a03e2-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="a03e2-115">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a03e2-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="a03e2-116">Пример 2: обновление режима определения политики</span><span class="sxs-lookup"><span data-stu-id="a03e2-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="a03e2-117">Эта команда обновляет определение политики с именем VMPolicyDefinition с помощью командлета Set-AzPolicyDefinition, чтобы установить для свойства Mode значение ALL.</span><span class="sxs-lookup"><span data-stu-id="a03e2-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="a03e2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a03e2-118">PARAMETERS</span></span>

### <span data-ttu-id="a03e2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a03e2-119">-ApiVersion</span></span>
<span data-ttu-id="a03e2-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a03e2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a03e2-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a03e2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a03e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03e2-122">-DefaultProfile</span></span>
<span data-ttu-id="a03e2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a03e2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03e2-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="a03e2-124">-Description</span></span>
<span data-ttu-id="a03e2-125">Задает новое описание для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="a03e2-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a03e2-126">-DisplayName</span></span>
<span data-ttu-id="a03e2-127">Задает новое отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="a03e2-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a03e2-128">-Id</span></span>
<span data-ttu-id="a03e2-129">Указывает полный идентификатор ресурса для определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a03e2-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03e2-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a03e2-130">-InformationAction</span></span>
<span data-ttu-id="a03e2-131">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a03e2-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a03e2-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a03e2-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a03e2-133">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a03e2-133">Continue</span></span>
- <span data-ttu-id="a03e2-134">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a03e2-134">Ignore</span></span>
- <span data-ttu-id="a03e2-135">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a03e2-135">Inquire</span></span>
- <span data-ttu-id="a03e2-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a03e2-136">SilentlyContinue</span></span>
- <span data-ttu-id="a03e2-137">Остановить</span><span class="sxs-lookup"><span data-stu-id="a03e2-137">Stop</span></span>
- <span data-ttu-id="a03e2-138">Рвать</span><span class="sxs-lookup"><span data-stu-id="a03e2-138">Suspend</span></span>

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

### <span data-ttu-id="a03e2-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a03e2-139">-InformationVariable</span></span>
<span data-ttu-id="a03e2-140">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a03e2-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a03e2-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a03e2-141">-ManagementGroupName</span></span>
<span data-ttu-id="a03e2-142">Имя группы управления для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="a03e2-142">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03e2-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a03e2-143">-Metadata</span></span>
<span data-ttu-id="a03e2-144">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-144">The metadata for policy definition.</span></span> <span data-ttu-id="a03e2-145">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a03e2-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="a03e2-146">Режим</span><span class="sxs-lookup"><span data-stu-id="a03e2-146">-Mode</span></span>
<span data-ttu-id="a03e2-147">Режим нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="a03e2-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a03e2-148">-Name</span></span>
<span data-ttu-id="a03e2-149">Указывает имя определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a03e2-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03e2-150">-Параметр</span><span class="sxs-lookup"><span data-stu-id="a03e2-150">-Parameter</span></span>
<span data-ttu-id="a03e2-151">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a03e2-152">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявлению параметров в виде String.</span><span class="sxs-lookup"><span data-stu-id="a03e2-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a03e2-153">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a03e2-153">-Policy</span></span>
<span data-ttu-id="a03e2-154">Задает новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a03e2-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="a03e2-155">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="a03e2-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a03e2-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="a03e2-156">-Pre</span></span>
<span data-ttu-id="a03e2-157">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a03e2-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a03e2-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a03e2-158">-SubscriptionId</span></span>
<span data-ttu-id="a03e2-159">Идентификатор подписки для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="a03e2-159">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03e2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03e2-160">CommonParameters</span></span>
<span data-ttu-id="a03e2-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a03e2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03e2-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03e2-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03e2-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a03e2-163">INPUTS</span></span>

## <span data-ttu-id="a03e2-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a03e2-164">OUTPUTS</span></span>

## <span data-ttu-id="a03e2-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="a03e2-165">NOTES</span></span>

## <span data-ttu-id="a03e2-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a03e2-166">RELATED LINKS</span></span>

[<span data-ttu-id="a03e2-167">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a03e2-167">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a03e2-168">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a03e2-168">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a03e2-169">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a03e2-169">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


