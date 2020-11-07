---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912315"
---
# <span data-ttu-id="47eba-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="47eba-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="47eba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47eba-102">SYNOPSIS</span></span>
<span data-ttu-id="47eba-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="47eba-103">Gets a resource lock.</span></span>

## <span data-ttu-id="47eba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47eba-104">SYNTAX</span></span>

### <span data-ttu-id="47eba-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47eba-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47eba-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="47eba-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47eba-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="47eba-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47eba-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="47eba-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47eba-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="47eba-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47eba-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="47eba-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47eba-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="47eba-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47eba-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47eba-112">DESCRIPTION</span></span>
<span data-ttu-id="47eba-113">Командлет **Get-AzResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="47eba-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="47eba-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47eba-114">EXAMPLES</span></span>

### <span data-ttu-id="47eba-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="47eba-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="47eba-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="47eba-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="47eba-117">Пример 2: получение блокировок на уровне группы ресурсов или более высоком</span><span class="sxs-lookup"><span data-stu-id="47eba-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="47eba-118">Эта команда получает блокировки ресурса для группы ресурсов или подписки.</span><span class="sxs-lookup"><span data-stu-id="47eba-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="47eba-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47eba-119">PARAMETERS</span></span>

### <span data-ttu-id="47eba-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47eba-120">-ApiVersion</span></span>
<span data-ttu-id="47eba-121">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47eba-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="47eba-122">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="47eba-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="47eba-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="47eba-123">-AtScope</span></span>
<span data-ttu-id="47eba-124">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="47eba-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="47eba-125">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="47eba-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="47eba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47eba-126">-DefaultProfile</span></span>
<span data-ttu-id="47eba-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47eba-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47eba-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="47eba-128">-LockId</span></span>
<span data-ttu-id="47eba-129">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="47eba-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="47eba-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="47eba-130">-LockName</span></span>
<span data-ttu-id="47eba-131">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="47eba-131">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="47eba-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="47eba-132">-Pre</span></span>
<span data-ttu-id="47eba-133">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="47eba-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="47eba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47eba-134">-ResourceGroupName</span></span>
<span data-ttu-id="47eba-135">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="47eba-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="47eba-136">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47eba-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="47eba-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47eba-137">-ResourceName</span></span>
<span data-ttu-id="47eba-138">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="47eba-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="47eba-139">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="47eba-139">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="47eba-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="47eba-140">-ResourceType</span></span>
<span data-ttu-id="47eba-141">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="47eba-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="47eba-142">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="47eba-142">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="47eba-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="47eba-143">-Scope</span></span>
<span data-ttu-id="47eba-144">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="47eba-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="47eba-145">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="47eba-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="47eba-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="47eba-146">-TenantLevel</span></span>
<span data-ttu-id="47eba-147">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="47eba-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="47eba-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47eba-148">CommonParameters</span></span>
<span data-ttu-id="47eba-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47eba-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47eba-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47eba-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47eba-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47eba-151">INPUTS</span></span>

### <span data-ttu-id="47eba-152">System. String</span><span class="sxs-lookup"><span data-stu-id="47eba-152">System.String</span></span>

## <span data-ttu-id="47eba-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47eba-153">OUTPUTS</span></span>

### <span data-ttu-id="47eba-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="47eba-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="47eba-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="47eba-155">NOTES</span></span>

## <span data-ttu-id="47eba-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47eba-156">RELATED LINKS</span></span>

[<span data-ttu-id="47eba-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="47eba-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="47eba-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="47eba-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="47eba-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="47eba-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


