---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: e3d0dfe975a6a76267864b329c3e3130f447cb58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557195"
---
# <span data-ttu-id="f5f42-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5f42-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="f5f42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5f42-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f42-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5f42-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5f42-104">SYNTAX</span></span>

### <span data-ttu-id="f5f42-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5f42-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f5f42-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f5f42-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f5f42-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f5f42-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f5f42-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5f42-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f5f42-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f5f42-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f42-112">DESCRIPTION</span></span>
<span data-ttu-id="f5f42-113">Командлет **Get-AzureRmResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f42-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f5f42-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5f42-114">EXAMPLES</span></span>

### <span data-ttu-id="f5f42-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="f5f42-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f5f42-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="f5f42-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f5f42-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5f42-117">PARAMETERS</span></span>

### <span data-ttu-id="f5f42-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5f42-118">-ApiVersion</span></span>
<span data-ttu-id="f5f42-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5f42-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5f42-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="f5f42-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f5f42-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f5f42-121">-AtScope</span></span>
<span data-ttu-id="f5f42-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f5f42-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f5f42-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="f5f42-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f5f42-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f42-124">-DefaultProfile</span></span>
<span data-ttu-id="f5f42-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5f42-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5f42-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f5f42-126">-InformationAction</span></span>
<span data-ttu-id="f5f42-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f5f42-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5f42-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f5f42-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5f42-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f5f42-129">Continue</span></span>
- <span data-ttu-id="f5f42-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f5f42-130">Ignore</span></span>
- <span data-ttu-id="f5f42-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f5f42-131">Inquire</span></span>
- <span data-ttu-id="f5f42-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5f42-132">SilentlyContinue</span></span>
- <span data-ttu-id="f5f42-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="f5f42-133">Stop</span></span>
- <span data-ttu-id="f5f42-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="f5f42-134">Suspend</span></span>

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

### <span data-ttu-id="f5f42-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5f42-135">-InformationVariable</span></span>
<span data-ttu-id="f5f42-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f5f42-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f5f42-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="f5f42-137">-LockId</span></span>
<span data-ttu-id="f5f42-138">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5f42-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="f5f42-139">-LockName</span></span>
<span data-ttu-id="f5f42-140">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5f42-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5f42-141">-Pre</span></span>
<span data-ttu-id="f5f42-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f5f42-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5f42-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f42-143">-ResourceGroupName</span></span>
<span data-ttu-id="f5f42-144">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5f42-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f5f42-145">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5f42-145">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f5f42-146">-ResourceName</span></span>
<span data-ttu-id="f5f42-147">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5f42-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f5f42-148">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5f42-148">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f5f42-149">-ResourceType</span></span>
<span data-ttu-id="f5f42-150">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5f42-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f5f42-151">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5f42-151">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="f5f42-152">-Scope</span></span>
<span data-ttu-id="f5f42-153">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5f42-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f5f42-154">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="f5f42-154">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f5f42-155">-TenantLevel</span></span>
<span data-ttu-id="f5f42-156">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="f5f42-156">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f42-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f42-157">CommonParameters</span></span>
<span data-ttu-id="f5f42-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5f42-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f42-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f42-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f42-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5f42-160">INPUTS</span></span>

### <span data-ttu-id="f5f42-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5f42-161">None</span></span>
<span data-ttu-id="f5f42-162">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f5f42-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5f42-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f42-163">OUTPUTS</span></span>

### <span data-ttu-id="f5f42-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5f42-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5f42-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5f42-165">NOTES</span></span>

## <span data-ttu-id="f5f42-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5f42-166">RELATED LINKS</span></span>

[<span data-ttu-id="f5f42-167">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5f42-167">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="f5f42-168">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5f42-168">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="f5f42-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5f42-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


