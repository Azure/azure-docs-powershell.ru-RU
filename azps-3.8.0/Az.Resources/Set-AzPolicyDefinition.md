---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066207"
---
# <span data-ttu-id="ccdba-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ccdba-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="ccdba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccdba-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdba-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="ccdba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccdba-104">SYNTAX</span></span>

### <span data-ttu-id="ccdba-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccdba-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccdba-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccdba-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccdba-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccdba-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccdba-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccdba-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccdba-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccdba-109">DESCRIPTION</span></span>
<span data-ttu-id="ccdba-110">Командлет **Set-AzPolicyDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ccdba-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccdba-111">EXAMPLES</span></span>

### <span data-ttu-id="ccdba-112">Пример 1: Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="ccdba-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="ccdba-113">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ccdba-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ccdba-114">Команда сохраняет этот объект в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ccdba-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="ccdba-115">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ccdba-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="ccdba-116">Пример 2: обновление режима определения политики</span><span class="sxs-lookup"><span data-stu-id="ccdba-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="ccdba-117">Эта команда обновляет определение политики с именем VMPolicyDefinition с помощью командлета Set-AzPolicyDefinition, чтобы установить для свойства Mode значение ALL.</span><span class="sxs-lookup"><span data-stu-id="ccdba-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="ccdba-118">Пример 3: обновление метаданных определения политики</span><span class="sxs-lookup"><span data-stu-id="ccdba-118">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="ccdba-119">Эта команда обновляет метаданные определения политики с именем VMPolicyDefinition, чтобы указать, что ее Категория — "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="ccdba-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="ccdba-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccdba-120">PARAMETERS</span></span>

### <span data-ttu-id="ccdba-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ccdba-121">-ApiVersion</span></span>
<span data-ttu-id="ccdba-122">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ccdba-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ccdba-123">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ccdba-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ccdba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdba-124">-DefaultProfile</span></span>
<span data-ttu-id="ccdba-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ccdba-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccdba-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="ccdba-126">-Description</span></span>
<span data-ttu-id="ccdba-127">Задает новое описание для определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="ccdba-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ccdba-128">-DisplayName</span></span>
<span data-ttu-id="ccdba-129">Задает новое отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="ccdba-130">-ID</span><span class="sxs-lookup"><span data-stu-id="ccdba-130">-Id</span></span>
<span data-ttu-id="ccdba-131">Указывает полный идентификатор ресурса для определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ccdba-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ccdba-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdba-132">-ManagementGroupName</span></span>
<span data-ttu-id="ccdba-133">Имя группы управления для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ccdba-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="ccdba-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ccdba-134">-Metadata</span></span>
<span data-ttu-id="ccdba-135">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-135">The metadata for policy definition.</span></span> <span data-ttu-id="ccdba-136">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ccdba-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="ccdba-137">Режим</span><span class="sxs-lookup"><span data-stu-id="ccdba-137">-Mode</span></span>
<span data-ttu-id="ccdba-138">Режим нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="ccdba-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccdba-139">-Name</span></span>
<span data-ttu-id="ccdba-140">Указывает имя определения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ccdba-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ccdba-141">-Параметр</span><span class="sxs-lookup"><span data-stu-id="ccdba-141">-Parameter</span></span>
<span data-ttu-id="ccdba-142">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="ccdba-143">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявлению параметров в виде String.</span><span class="sxs-lookup"><span data-stu-id="ccdba-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="ccdba-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="ccdba-144">-Policy</span></span>
<span data-ttu-id="ccdba-145">Задает новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="ccdba-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="ccdba-146">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="ccdba-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="ccdba-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="ccdba-147">-Pre</span></span>
<span data-ttu-id="ccdba-148">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ccdba-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ccdba-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccdba-149">-SubscriptionId</span></span>
<span data-ttu-id="ccdba-150">Идентификатор подписки для определения политики, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ccdba-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="ccdba-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdba-151">CommonParameters</span></span>
<span data-ttu-id="ccdba-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccdba-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdba-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccdba-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdba-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccdba-154">INPUTS</span></span>

### <span data-ttu-id="ccdba-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ccdba-155">System.String</span></span>

### <span data-ttu-id="ccdba-156">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ccdba-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ccdba-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccdba-157">OUTPUTS</span></span>

### <span data-ttu-id="ccdba-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ccdba-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ccdba-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccdba-159">NOTES</span></span>

## <span data-ttu-id="ccdba-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccdba-160">RELATED LINKS</span></span>

[<span data-ttu-id="ccdba-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ccdba-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="ccdba-162">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ccdba-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="ccdba-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ccdba-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


