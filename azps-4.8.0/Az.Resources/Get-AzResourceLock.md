---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236644"
---
# <span data-ttu-id="f5c1a-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5c1a-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="f5c1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c1a-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-103">Gets a resource lock.</span></span>

## <span data-ttu-id="f5c1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5c1a-104">SYNTAX</span></span>

### <span data-ttu-id="f5c1a-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5c1a-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c1a-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f5c1a-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5c1a-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f5c1a-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c1a-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f5c1a-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c1a-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f5c1a-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c1a-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f5c1a-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c1a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5c1a-111">DESCRIPTION</span></span>
<span data-ttu-id="f5c1a-112">Командлет **Get-AzResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f5c1a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5c1a-113">EXAMPLES</span></span>

### <span data-ttu-id="f5c1a-114">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="f5c1a-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f5c1a-115">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="f5c1a-116">Пример 2: получение блокировок на уровне группы ресурсов или более высоком</span><span class="sxs-lookup"><span data-stu-id="f5c1a-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="f5c1a-117">Эта команда получает блокировки ресурса для группы ресурсов или подписки.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="f5c1a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5c1a-118">PARAMETERS</span></span>

### <span data-ttu-id="f5c1a-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5c1a-119">-ApiVersion</span></span>
<span data-ttu-id="f5c1a-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5c1a-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f5c1a-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f5c1a-122">-AtScope</span></span>
<span data-ttu-id="f5c1a-123">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f5c1a-124">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f5c1a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c1a-125">-DefaultProfile</span></span>
<span data-ttu-id="f5c1a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5c1a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5c1a-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="f5c1a-127">-LockId</span></span>
<span data-ttu-id="f5c1a-128">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5c1a-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="f5c1a-129">-LockName</span></span>
<span data-ttu-id="f5c1a-130">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5c1a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5c1a-131">-Pre</span></span>
<span data-ttu-id="f5c1a-132">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5c1a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c1a-133">-ResourceGroupName</span></span>
<span data-ttu-id="f5c1a-134">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f5c1a-135">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="f5c1a-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f5c1a-136">-ResourceName</span></span>
<span data-ttu-id="f5c1a-137">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f5c1a-138">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f5c1a-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f5c1a-139">-ResourceType</span></span>
<span data-ttu-id="f5c1a-140">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f5c1a-141">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f5c1a-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="f5c1a-142">-Scope</span></span>
<span data-ttu-id="f5c1a-143">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f5c1a-144">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="f5c1a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c1a-145">CommonParameters</span></span>
<span data-ttu-id="f5c1a-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5c1a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c1a-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5c1a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c1a-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5c1a-148">INPUTS</span></span>

### <span data-ttu-id="f5c1a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c1a-149">System.String</span></span>

## <span data-ttu-id="f5c1a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5c1a-150">OUTPUTS</span></span>

### <span data-ttu-id="f5c1a-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5c1a-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5c1a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5c1a-152">NOTES</span></span>

## <span data-ttu-id="f5c1a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5c1a-153">RELATED LINKS</span></span>

[<span data-ttu-id="f5c1a-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5c1a-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f5c1a-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5c1a-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f5c1a-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f5c1a-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


