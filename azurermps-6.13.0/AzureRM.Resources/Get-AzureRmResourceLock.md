---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 9681a88a1a4768617383a25122a0224ae264e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564044"
---
# <span data-ttu-id="245ff-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="245ff-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="245ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="245ff-102">SYNOPSIS</span></span>
<span data-ttu-id="245ff-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="245ff-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="245ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="245ff-104">SYNTAX</span></span>

### <span data-ttu-id="245ff-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="245ff-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="245ff-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="245ff-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="245ff-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="245ff-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="245ff-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="245ff-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="245ff-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="245ff-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="245ff-112">DESCRIPTION</span></span>
<span data-ttu-id="245ff-113">Командлет **Get-AzureRmResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="245ff-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="245ff-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="245ff-114">EXAMPLES</span></span>

### <span data-ttu-id="245ff-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="245ff-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="245ff-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="245ff-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="245ff-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="245ff-117">PARAMETERS</span></span>

### <span data-ttu-id="245ff-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="245ff-118">-ApiVersion</span></span>
<span data-ttu-id="245ff-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="245ff-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="245ff-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="245ff-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="245ff-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="245ff-121">-AtScope</span></span>
<span data-ttu-id="245ff-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="245ff-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="245ff-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="245ff-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="245ff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245ff-124">-DefaultProfile</span></span>
<span data-ttu-id="245ff-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="245ff-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="245ff-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="245ff-126">-InformationAction</span></span>
<span data-ttu-id="245ff-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="245ff-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="245ff-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="245ff-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="245ff-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="245ff-129">Continue</span></span>
- <span data-ttu-id="245ff-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="245ff-130">Ignore</span></span>
- <span data-ttu-id="245ff-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="245ff-131">Inquire</span></span>
- <span data-ttu-id="245ff-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="245ff-132">SilentlyContinue</span></span>
- <span data-ttu-id="245ff-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="245ff-133">Stop</span></span>
- <span data-ttu-id="245ff-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="245ff-134">Suspend</span></span>

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

### <span data-ttu-id="245ff-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="245ff-135">-InformationVariable</span></span>
<span data-ttu-id="245ff-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="245ff-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="245ff-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="245ff-137">-LockId</span></span>
<span data-ttu-id="245ff-138">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="245ff-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="245ff-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="245ff-139">-LockName</span></span>
<span data-ttu-id="245ff-140">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="245ff-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="245ff-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="245ff-141">-Pre</span></span>
<span data-ttu-id="245ff-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="245ff-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="245ff-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245ff-143">-ResourceGroupName</span></span>
<span data-ttu-id="245ff-144">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="245ff-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="245ff-145">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="245ff-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="245ff-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="245ff-146">-ResourceName</span></span>
<span data-ttu-id="245ff-147">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="245ff-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="245ff-148">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="245ff-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="245ff-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="245ff-149">-ResourceType</span></span>
<span data-ttu-id="245ff-150">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="245ff-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="245ff-151">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="245ff-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="245ff-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="245ff-152">-Scope</span></span>
<span data-ttu-id="245ff-153">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="245ff-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="245ff-154">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="245ff-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="245ff-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="245ff-155">-TenantLevel</span></span>
<span data-ttu-id="245ff-156">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="245ff-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="245ff-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245ff-157">CommonParameters</span></span>
<span data-ttu-id="245ff-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="245ff-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245ff-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245ff-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245ff-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="245ff-160">INPUTS</span></span>

## <span data-ttu-id="245ff-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="245ff-161">OUTPUTS</span></span>

## <span data-ttu-id="245ff-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="245ff-162">NOTES</span></span>

## <span data-ttu-id="245ff-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="245ff-163">RELATED LINKS</span></span>

[<span data-ttu-id="245ff-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="245ff-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="245ff-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="245ff-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="245ff-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="245ff-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


