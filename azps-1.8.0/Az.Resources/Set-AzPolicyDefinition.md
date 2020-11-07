---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729315"
---
# <span data-ttu-id="c2604-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2604-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="c2604-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2604-102">SYNOPSIS</span></span>
<span data-ttu-id="c2604-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="c2604-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2604-104">SYNTAX</span></span>

### <span data-ttu-id="c2604-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2604-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2604-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2604-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2604-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2604-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2604-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2604-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2604-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2604-109">DESCRIPTION</span></span>
<span data-ttu-id="c2604-110">Командлет **Set-AzPolicyDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c2604-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2604-111">EXAMPLES</span></span>

### <span data-ttu-id="c2604-112">Пример 1: Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="c2604-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="c2604-113">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c2604-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c2604-114">Команда сохраняет этот объект в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c2604-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="c2604-115">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c2604-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="c2604-116">Пример 2: обновление режима определения политики</span><span class="sxs-lookup"><span data-stu-id="c2604-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="c2604-117">Эта команда обновляет определение политики с именем VMPolicyDefinition с помощью командлета Set-AzPolicyDefinition, чтобы установить для свойства Mode значение ALL.</span><span class="sxs-lookup"><span data-stu-id="c2604-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="c2604-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2604-118">PARAMETERS</span></span>

### <span data-ttu-id="c2604-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2604-119">-ApiVersion</span></span>
<span data-ttu-id="c2604-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2604-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2604-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="c2604-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c2604-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2604-122">-DefaultProfile</span></span>
<span data-ttu-id="c2604-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2604-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2604-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="c2604-124">-Description</span></span>
<span data-ttu-id="c2604-125">Задает новое описание для определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="c2604-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2604-126">-DisplayName</span></span>
<span data-ttu-id="c2604-127">Задает новое отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="c2604-128">-ID</span><span class="sxs-lookup"><span data-stu-id="c2604-128">-Id</span></span>
<span data-ttu-id="c2604-129">Указывает полный идентификатор ресурса для определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c2604-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c2604-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c2604-130">-ManagementGroupName</span></span>
<span data-ttu-id="c2604-131">Имя группы управления для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="c2604-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="c2604-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c2604-132">-Metadata</span></span>
<span data-ttu-id="c2604-133">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-133">The metadata for policy definition.</span></span> <span data-ttu-id="c2604-134">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c2604-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="c2604-135">Режим</span><span class="sxs-lookup"><span data-stu-id="c2604-135">-Mode</span></span>
<span data-ttu-id="c2604-136">Режим нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="c2604-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2604-137">-Name</span></span>
<span data-ttu-id="c2604-138">Указывает имя определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c2604-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c2604-139">-Параметр</span><span class="sxs-lookup"><span data-stu-id="c2604-139">-Parameter</span></span>
<span data-ttu-id="c2604-140">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="c2604-141">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявлению параметров в виде String.</span><span class="sxs-lookup"><span data-stu-id="c2604-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="c2604-142">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c2604-142">-Policy</span></span>
<span data-ttu-id="c2604-143">Задает новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="c2604-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="c2604-144">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="c2604-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c2604-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2604-145">-Pre</span></span>
<span data-ttu-id="c2604-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="c2604-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c2604-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2604-147">-SubscriptionId</span></span>
<span data-ttu-id="c2604-148">Идентификатор подписки для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="c2604-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="c2604-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2604-149">CommonParameters</span></span>
<span data-ttu-id="c2604-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2604-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2604-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2604-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2604-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2604-152">INPUTS</span></span>

### <span data-ttu-id="c2604-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c2604-153">System.String</span></span>

### <span data-ttu-id="c2604-154">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c2604-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c2604-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2604-155">OUTPUTS</span></span>

### <span data-ttu-id="c2604-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c2604-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c2604-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2604-157">NOTES</span></span>

## <span data-ttu-id="c2604-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2604-158">RELATED LINKS</span></span>

[<span data-ttu-id="c2604-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2604-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c2604-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2604-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="c2604-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2604-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


