---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734239"
---
# <span data-ttu-id="71a77-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71a77-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="71a77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71a77-102">SYNOPSIS</span></span>
<span data-ttu-id="71a77-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="71a77-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71a77-104">SYNTAX</span></span>

### <span data-ttu-id="71a77-105">Заданный параметр имени определения политики.</span><span class="sxs-lookup"><span data-stu-id="71a77-105">The policy definition name parameter set.</span></span> <span data-ttu-id="71a77-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="71a77-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a77-107">Заданный параметр идентификатора определения политики.</span><span class="sxs-lookup"><span data-stu-id="71a77-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a77-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a77-108">DESCRIPTION</span></span>
<span data-ttu-id="71a77-109">Командлет **Remove-AzureRmPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="71a77-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="71a77-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71a77-110">EXAMPLES</span></span>

### <span data-ttu-id="71a77-111">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="71a77-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="71a77-112">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="71a77-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="71a77-113">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="71a77-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="71a77-114">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71a77-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="71a77-115">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71a77-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="71a77-116">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71a77-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="71a77-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71a77-117">PARAMETERS</span></span>

### <span data-ttu-id="71a77-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71a77-118">-ApiVersion</span></span>
<span data-ttu-id="71a77-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71a77-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="71a77-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="71a77-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="71a77-121">-Force</span><span class="sxs-lookup"><span data-stu-id="71a77-121">-Force</span></span>
<span data-ttu-id="71a77-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="71a77-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71a77-123">-ID</span><span class="sxs-lookup"><span data-stu-id="71a77-123">-Id</span></span>
<span data-ttu-id="71a77-124">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71a77-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71a77-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71a77-125">-InformationAction</span></span>
<span data-ttu-id="71a77-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="71a77-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71a77-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="71a77-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71a77-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="71a77-128">Continue</span></span>
- <span data-ttu-id="71a77-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="71a77-129">Ignore</span></span>
- <span data-ttu-id="71a77-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="71a77-130">Inquire</span></span>
- <span data-ttu-id="71a77-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71a77-131">SilentlyContinue</span></span>
- <span data-ttu-id="71a77-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="71a77-132">Stop</span></span>
- <span data-ttu-id="71a77-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="71a77-133">Suspend</span></span>

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

### <span data-ttu-id="71a77-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71a77-134">-InformationVariable</span></span>
<span data-ttu-id="71a77-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="71a77-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71a77-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71a77-136">-Name</span></span>
<span data-ttu-id="71a77-137">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71a77-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71a77-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="71a77-138">-Pre</span></span>
<span data-ttu-id="71a77-139">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="71a77-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71a77-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a77-140">-Confirm</span></span>
<span data-ttu-id="71a77-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71a77-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a77-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a77-142">-WhatIf</span></span>
<span data-ttu-id="71a77-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71a77-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a77-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71a77-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a77-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a77-145">-DefaultProfile</span></span>
<span data-ttu-id="71a77-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71a77-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71a77-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a77-147">CommonParameters</span></span>
<span data-ttu-id="71a77-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71a77-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a77-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a77-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a77-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71a77-150">INPUTS</span></span>

## <span data-ttu-id="71a77-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a77-151">OUTPUTS</span></span>

### <span data-ttu-id="71a77-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71a77-152">System.Boolean</span></span>

## <span data-ttu-id="71a77-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="71a77-153">NOTES</span></span>

## <span data-ttu-id="71a77-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71a77-154">RELATED LINKS</span></span>

[<span data-ttu-id="71a77-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71a77-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71a77-156">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71a77-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71a77-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71a77-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


