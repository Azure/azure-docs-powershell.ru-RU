---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: e774b333703714246de852d3f72ba704d7122b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910930"
---
# <span data-ttu-id="ef094-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ef094-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="ef094-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef094-102">SYNOPSIS</span></span>
<span data-ttu-id="ef094-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef094-103">Gets a resource lock.</span></span>

## <span data-ttu-id="ef094-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef094-104">SYNTAX</span></span>

### <span data-ttu-id="ef094-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef094-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="ef094-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="ef094-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ef094-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ef094-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef094-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef094-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="ef094-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef094-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef094-112">DESCRIPTION</span></span>
<span data-ttu-id="ef094-113">Командлет **Get-AzResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ef094-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="ef094-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef094-114">EXAMPLES</span></span>

### <span data-ttu-id="ef094-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="ef094-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ef094-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="ef094-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="ef094-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef094-117">PARAMETERS</span></span>

### <span data-ttu-id="ef094-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef094-118">-ApiVersion</span></span>
<span data-ttu-id="ef094-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef094-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef094-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ef094-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef094-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="ef094-121">-AtScope</span></span>
<span data-ttu-id="ef094-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ef094-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="ef094-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="ef094-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="ef094-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef094-124">-DefaultProfile</span></span>
<span data-ttu-id="ef094-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ef094-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef094-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ef094-126">-InformationAction</span></span>
<span data-ttu-id="ef094-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ef094-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ef094-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ef094-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef094-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ef094-129">Continue</span></span>
- <span data-ttu-id="ef094-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ef094-130">Ignore</span></span>
- <span data-ttu-id="ef094-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ef094-131">Inquire</span></span>
- <span data-ttu-id="ef094-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef094-132">SilentlyContinue</span></span>
- <span data-ttu-id="ef094-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="ef094-133">Stop</span></span>
- <span data-ttu-id="ef094-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="ef094-134">Suspend</span></span>

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

### <span data-ttu-id="ef094-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef094-135">-InformationVariable</span></span>
<span data-ttu-id="ef094-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ef094-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ef094-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="ef094-137">-LockId</span></span>
<span data-ttu-id="ef094-138">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef094-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="ef094-139">-LockName</span></span>
<span data-ttu-id="ef094-140">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef094-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef094-141">-Pre</span></span>
<span data-ttu-id="ef094-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ef094-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef094-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef094-143">-ResourceGroupName</span></span>
<span data-ttu-id="ef094-144">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ef094-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="ef094-145">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef094-145">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef094-146">-ResourceName</span></span>
<span data-ttu-id="ef094-147">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="ef094-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="ef094-148">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef094-148">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef094-149">-ResourceType</span></span>
<span data-ttu-id="ef094-150">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="ef094-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="ef094-151">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef094-151">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="ef094-152">-Scope</span></span>
<span data-ttu-id="ef094-153">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ef094-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="ef094-154">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="ef094-154">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef094-155">-TenantLevel</span></span>
<span data-ttu-id="ef094-156">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="ef094-156">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef094-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef094-157">CommonParameters</span></span>
<span data-ttu-id="ef094-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef094-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef094-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef094-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef094-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef094-160">INPUTS</span></span>

## <span data-ttu-id="ef094-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef094-161">OUTPUTS</span></span>

## <span data-ttu-id="ef094-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef094-162">NOTES</span></span>

## <span data-ttu-id="ef094-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef094-163">RELATED LINKS</span></span>

[<span data-ttu-id="ef094-164">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ef094-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="ef094-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ef094-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="ef094-166">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ef094-166">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


