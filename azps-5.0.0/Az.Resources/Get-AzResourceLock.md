---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316408"
---
# <span data-ttu-id="5920d-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5920d-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="5920d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5920d-102">SYNOPSIS</span></span>
<span data-ttu-id="5920d-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="5920d-103">Gets a resource lock.</span></span>

## <span data-ttu-id="5920d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5920d-104">SYNTAX</span></span>

### <span data-ttu-id="5920d-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5920d-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5920d-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="5920d-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5920d-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="5920d-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5920d-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5920d-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5920d-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5920d-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5920d-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="5920d-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5920d-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5920d-111">DESCRIPTION</span></span>
<span data-ttu-id="5920d-112">Командлет **Get-AzResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5920d-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="5920d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5920d-113">EXAMPLES</span></span>

### <span data-ttu-id="5920d-114">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="5920d-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5920d-115">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="5920d-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="5920d-116">Пример 2: получение блокировок на уровне группы ресурсов или более высоком</span><span class="sxs-lookup"><span data-stu-id="5920d-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="5920d-117">Эта команда получает блокировки ресурса для группы ресурсов или подписки.</span><span class="sxs-lookup"><span data-stu-id="5920d-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="5920d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5920d-118">PARAMETERS</span></span>

### <span data-ttu-id="5920d-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5920d-119">-ApiVersion</span></span>
<span data-ttu-id="5920d-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5920d-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5920d-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="5920d-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5920d-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="5920d-122">-AtScope</span></span>
<span data-ttu-id="5920d-123">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5920d-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="5920d-124">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="5920d-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="5920d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5920d-125">-DefaultProfile</span></span>
<span data-ttu-id="5920d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5920d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5920d-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="5920d-127">-LockId</span></span>
<span data-ttu-id="5920d-128">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5920d-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5920d-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="5920d-129">-LockName</span></span>
<span data-ttu-id="5920d-130">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5920d-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5920d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="5920d-131">-Pre</span></span>
<span data-ttu-id="5920d-132">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="5920d-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5920d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5920d-133">-ResourceGroupName</span></span>
<span data-ttu-id="5920d-134">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="5920d-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="5920d-135">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5920d-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="5920d-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5920d-136">-ResourceName</span></span>
<span data-ttu-id="5920d-137">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="5920d-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="5920d-138">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="5920d-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5920d-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5920d-139">-ResourceType</span></span>
<span data-ttu-id="5920d-140">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="5920d-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="5920d-141">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="5920d-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5920d-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="5920d-142">-Scope</span></span>
<span data-ttu-id="5920d-143">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="5920d-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5920d-144">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="5920d-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="5920d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5920d-145">CommonParameters</span></span>
<span data-ttu-id="5920d-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5920d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5920d-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5920d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5920d-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5920d-148">INPUTS</span></span>

### <span data-ttu-id="5920d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5920d-149">System.String</span></span>

## <span data-ttu-id="5920d-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5920d-150">OUTPUTS</span></span>

### <span data-ttu-id="5920d-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5920d-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5920d-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="5920d-152">NOTES</span></span>

## <span data-ttu-id="5920d-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5920d-153">RELATED LINKS</span></span>

[<span data-ttu-id="5920d-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5920d-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="5920d-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5920d-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="5920d-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5920d-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


