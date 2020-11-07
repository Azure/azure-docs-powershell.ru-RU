---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729417"
---
# <span data-ttu-id="f3d0c-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3d0c-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="f3d0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d0c-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-103">Gets a resource lock.</span></span>

## <span data-ttu-id="f3d0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3d0c-104">SYNTAX</span></span>

### <span data-ttu-id="f3d0c-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3d0c-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f3d0c-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f3d0c-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f3d0c-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f3d0c-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3d0c-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d0c-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f3d0c-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d0c-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d0c-112">DESCRIPTION</span></span>
<span data-ttu-id="f3d0c-113">Командлет **Get-AzResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f3d0c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3d0c-114">EXAMPLES</span></span>

### <span data-ttu-id="f3d0c-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="f3d0c-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f3d0c-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f3d0c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3d0c-117">PARAMETERS</span></span>

### <span data-ttu-id="f3d0c-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3d0c-118">-ApiVersion</span></span>
<span data-ttu-id="f3d0c-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f3d0c-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f3d0c-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f3d0c-121">-AtScope</span></span>
<span data-ttu-id="f3d0c-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f3d0c-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f3d0c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d0c-124">-DefaultProfile</span></span>
<span data-ttu-id="f3d0c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f3d0c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3d0c-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="f3d0c-126">-LockId</span></span>
<span data-ttu-id="f3d0c-127">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3d0c-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="f3d0c-128">-LockName</span></span>
<span data-ttu-id="f3d0c-129">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3d0c-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3d0c-130">-Pre</span></span>
<span data-ttu-id="f3d0c-131">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3d0c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d0c-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3d0c-133">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f3d0c-134">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="f3d0c-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3d0c-135">-ResourceName</span></span>
<span data-ttu-id="f3d0c-136">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f3d0c-137">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f3d0c-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3d0c-138">-ResourceType</span></span>
<span data-ttu-id="f3d0c-139">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f3d0c-140">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f3d0c-141">-Scope</span><span class="sxs-lookup"><span data-stu-id="f3d0c-141">-Scope</span></span>
<span data-ttu-id="f3d0c-142">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f3d0c-143">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="f3d0c-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3d0c-144">-TenantLevel</span></span>
<span data-ttu-id="f3d0c-145">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f3d0c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d0c-146">CommonParameters</span></span>
<span data-ttu-id="f3d0c-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3d0c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d0c-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d0c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d0c-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3d0c-149">INPUTS</span></span>

### <span data-ttu-id="f3d0c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d0c-150">System.String</span></span>

## <span data-ttu-id="f3d0c-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d0c-151">OUTPUTS</span></span>

### <span data-ttu-id="f3d0c-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f3d0c-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f3d0c-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3d0c-153">NOTES</span></span>

## <span data-ttu-id="f3d0c-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3d0c-154">RELATED LINKS</span></span>

[<span data-ttu-id="f3d0c-155">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3d0c-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f3d0c-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3d0c-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f3d0c-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3d0c-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


