---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568311"
---
# <span data-ttu-id="4558c-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4558c-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4558c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4558c-102">SYNOPSIS</span></span>
<span data-ttu-id="4558c-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="4558c-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4558c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4558c-104">SYNTAX</span></span>

### <span data-ttu-id="4558c-105">Установленный список всех параметров определений политики.</span><span class="sxs-lookup"><span data-stu-id="4558c-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="4558c-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="4558c-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4558c-107">Заданный параметр имени определения политики.</span><span class="sxs-lookup"><span data-stu-id="4558c-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4558c-108">Заданный параметр идентификатора определения политики.</span><span class="sxs-lookup"><span data-stu-id="4558c-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4558c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4558c-109">DESCRIPTION</span></span>
<span data-ttu-id="4558c-110">Командлет **Get-AzureRmPolicyDefinition** получает все определения политик или определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="4558c-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="4558c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4558c-111">EXAMPLES</span></span>

### <span data-ttu-id="4558c-112">Пример 1: получение определения политики</span><span class="sxs-lookup"><span data-stu-id="4558c-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="4558c-113">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="4558c-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="4558c-114">Пример 2: получение определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="4558c-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="4558c-115">Эта команда получает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4558c-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="4558c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4558c-116">PARAMETERS</span></span>

### <span data-ttu-id="4558c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4558c-117">-ApiVersion</span></span>
<span data-ttu-id="4558c-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4558c-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4558c-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="4558c-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4558c-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4558c-120">-Id</span></span>
<span data-ttu-id="4558c-121">Указывает полный идентификатор ресурса для определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4558c-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4558c-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4558c-122">-InformationAction</span></span>
<span data-ttu-id="4558c-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4558c-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4558c-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4558c-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4558c-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4558c-125">Continue</span></span>
- <span data-ttu-id="4558c-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4558c-126">Ignore</span></span>
- <span data-ttu-id="4558c-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4558c-127">Inquire</span></span>
- <span data-ttu-id="4558c-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4558c-128">SilentlyContinue</span></span>
- <span data-ttu-id="4558c-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="4558c-129">Stop</span></span>
- <span data-ttu-id="4558c-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="4558c-130">Suspend</span></span>

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

### <span data-ttu-id="4558c-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4558c-131">-InformationVariable</span></span>
<span data-ttu-id="4558c-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4558c-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4558c-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4558c-133">-Name</span></span>
<span data-ttu-id="4558c-134">Указывает имя определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4558c-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4558c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="4558c-135">-Pre</span></span>
<span data-ttu-id="4558c-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="4558c-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4558c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4558c-137">-DefaultProfile</span></span>
<span data-ttu-id="4558c-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4558c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4558c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4558c-139">CommonParameters</span></span>
<span data-ttu-id="4558c-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4558c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4558c-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4558c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4558c-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4558c-142">INPUTS</span></span>

## <span data-ttu-id="4558c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4558c-143">OUTPUTS</span></span>

### <span data-ttu-id="4558c-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4558c-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4558c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4558c-145">NOTES</span></span>

## <span data-ttu-id="4558c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4558c-146">RELATED LINKS</span></span>

[<span data-ttu-id="4558c-147">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4558c-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4558c-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4558c-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4558c-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4558c-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


