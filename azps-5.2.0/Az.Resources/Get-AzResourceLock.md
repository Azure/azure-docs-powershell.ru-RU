---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398124"
---
# <span data-ttu-id="b2290-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b2290-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="b2290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2290-102">SYNOPSIS</span></span>
<span data-ttu-id="b2290-103">Блокировка ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2290-103">Gets a resource lock.</span></span>

## <span data-ttu-id="b2290-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2290-104">SYNTAX</span></span>

### <span data-ttu-id="b2290-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2290-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2290-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="b2290-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2290-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="b2290-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2290-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="b2290-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2290-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b2290-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2290-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="b2290-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2290-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2290-111">DESCRIPTION</span></span>
<span data-ttu-id="b2290-112">Для получения блокировки ресурсов Azure **возвращается cmdlet Get-AzResourceLock.**</span><span class="sxs-lookup"><span data-stu-id="b2290-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="b2290-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2290-113">EXAMPLES</span></span>

### <span data-ttu-id="b2290-114">Пример 1. Блокировка</span><span class="sxs-lookup"><span data-stu-id="b2290-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b2290-115">Эта команда получает блокировку ресурса ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="b2290-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="b2290-116">Пример 2. Блокировка на уровне группы ресурсов или более высокого уровня</span><span class="sxs-lookup"><span data-stu-id="b2290-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="b2290-117">Эта команда блокирует ресурсы для группы ресурсов или подписки.</span><span class="sxs-lookup"><span data-stu-id="b2290-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="b2290-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2290-118">PARAMETERS</span></span>

### <span data-ttu-id="b2290-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2290-119">-ApiVersion</span></span>
<span data-ttu-id="b2290-120">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2290-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b2290-121">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b2290-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b2290-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="b2290-122">-AtScope</span></span>
<span data-ttu-id="b2290-123">Указывает на то, что этот cmdlet возвращает все блокировки, которые не должны фиксироваться в указанной области.</span><span class="sxs-lookup"><span data-stu-id="b2290-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="b2290-124">Если этот параметр не задан, он возвращает все блокировки в диапазоне, выше или ниже.</span><span class="sxs-lookup"><span data-stu-id="b2290-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="b2290-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2290-125">-DefaultProfile</span></span>
<span data-ttu-id="b2290-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2290-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2290-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="b2290-127">-LockId</span></span>
<span data-ttu-id="b2290-128">Определяет код блокировки, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2290-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2290-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="b2290-129">-LockName</span></span>
<span data-ttu-id="b2290-130">Указывает имя блокировки, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2290-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2290-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2290-131">-Pre</span></span>
<span data-ttu-id="b2290-132">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="b2290-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b2290-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2290-133">-ResourceGroupName</span></span>
<span data-ttu-id="b2290-134">Имя группы ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="b2290-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="b2290-135">Этот cmdlet получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2290-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="b2290-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b2290-136">-ResourceName</span></span>
<span data-ttu-id="b2290-137">Указывает имя ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="b2290-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="b2290-138">Этот cmdlet получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2290-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="b2290-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b2290-139">-ResourceType</span></span>
<span data-ttu-id="b2290-140">Определяет тип ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="b2290-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="b2290-141">Этот cmdlet получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2290-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="b2290-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="b2290-142">-Scope</span></span>
<span data-ttu-id="b2290-143">Определяет область применения блокировки.</span><span class="sxs-lookup"><span data-stu-id="b2290-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="b2290-144">Этот cmdlet получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="b2290-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="b2290-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2290-145">CommonParameters</span></span>
<span data-ttu-id="b2290-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2290-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2290-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2290-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2290-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2290-148">INPUTS</span></span>

### <span data-ttu-id="b2290-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b2290-149">System.String</span></span>

## <span data-ttu-id="b2290-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2290-150">OUTPUTS</span></span>

### <span data-ttu-id="b2290-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b2290-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b2290-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2290-152">NOTES</span></span>

## <span data-ttu-id="b2290-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2290-153">RELATED LINKS</span></span>

[<span data-ttu-id="b2290-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b2290-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="b2290-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b2290-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="b2290-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b2290-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


