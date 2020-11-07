---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913971"
---
# <span data-ttu-id="88203-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="88203-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="88203-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88203-102">SYNOPSIS</span></span>
<span data-ttu-id="88203-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="88203-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88203-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88203-104">SYNTAX</span></span>

### <span data-ttu-id="88203-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88203-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="88203-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="88203-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="88203-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="88203-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="88203-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="88203-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="88203-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="88203-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88203-112">DESCRIPTION</span></span>
<span data-ttu-id="88203-113">Командлет **Get-AzureRmResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="88203-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="88203-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88203-114">EXAMPLES</span></span>

### <span data-ttu-id="88203-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="88203-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="88203-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="88203-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="88203-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88203-117">PARAMETERS</span></span>

### <span data-ttu-id="88203-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88203-118">-ApiVersion</span></span>
<span data-ttu-id="88203-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88203-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="88203-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="88203-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="88203-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="88203-121">-AtScope</span></span>
<span data-ttu-id="88203-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="88203-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="88203-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="88203-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="88203-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88203-124">-DefaultProfile</span></span>
<span data-ttu-id="88203-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="88203-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88203-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="88203-126">-InformationAction</span></span>
<span data-ttu-id="88203-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="88203-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="88203-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="88203-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88203-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="88203-129">Continue</span></span>
- <span data-ttu-id="88203-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="88203-130">Ignore</span></span>
- <span data-ttu-id="88203-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="88203-131">Inquire</span></span>
- <span data-ttu-id="88203-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88203-132">SilentlyContinue</span></span>
- <span data-ttu-id="88203-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="88203-133">Stop</span></span>
- <span data-ttu-id="88203-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="88203-134">Suspend</span></span>

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

### <span data-ttu-id="88203-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88203-135">-InformationVariable</span></span>
<span data-ttu-id="88203-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="88203-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88203-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="88203-137">-LockId</span></span>
<span data-ttu-id="88203-138">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88203-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="88203-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="88203-139">-LockName</span></span>
<span data-ttu-id="88203-140">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88203-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="88203-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="88203-141">-Pre</span></span>
<span data-ttu-id="88203-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="88203-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88203-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88203-143">-ResourceGroupName</span></span>
<span data-ttu-id="88203-144">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="88203-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="88203-145">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88203-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="88203-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="88203-146">-ResourceName</span></span>
<span data-ttu-id="88203-147">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="88203-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="88203-148">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="88203-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="88203-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="88203-149">-ResourceType</span></span>
<span data-ttu-id="88203-150">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="88203-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="88203-151">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="88203-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="88203-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="88203-152">-Scope</span></span>
<span data-ttu-id="88203-153">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="88203-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="88203-154">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="88203-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="88203-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="88203-155">-TenantLevel</span></span>
<span data-ttu-id="88203-156">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="88203-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="88203-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88203-157">CommonParameters</span></span>
<span data-ttu-id="88203-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88203-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88203-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88203-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88203-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88203-160">INPUTS</span></span>

## <span data-ttu-id="88203-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88203-161">OUTPUTS</span></span>

## <span data-ttu-id="88203-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="88203-162">NOTES</span></span>

## <span data-ttu-id="88203-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88203-163">RELATED LINKS</span></span>

[<span data-ttu-id="88203-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="88203-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="88203-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="88203-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="88203-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="88203-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


