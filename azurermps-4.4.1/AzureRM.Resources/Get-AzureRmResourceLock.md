---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567079"
---
# <span data-ttu-id="87bbf-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87bbf-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="87bbf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="87bbf-103">Возвращает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="87bbf-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87bbf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87bbf-104">SYNTAX</span></span>

### <span data-ttu-id="87bbf-105">Блокировка в области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87bbf-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-106">Блокировка в области ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="87bbf-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-107">Блокировка на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="87bbf-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-108">Блокировка в области подписки.</span><span class="sxs-lookup"><span data-stu-id="87bbf-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-109">Блокировка в области ресурсов подписки.</span><span class="sxs-lookup"><span data-stu-id="87bbf-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-110">Блокировка в области ресурсов клиента.</span><span class="sxs-lookup"><span data-stu-id="87bbf-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87bbf-111">Блокировка по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="87bbf-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87bbf-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bbf-112">DESCRIPTION</span></span>
<span data-ttu-id="87bbf-113">Командлет **Get-AzureRmResourceLock** получает блокировки ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="87bbf-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="87bbf-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87bbf-114">EXAMPLES</span></span>

### <span data-ttu-id="87bbf-115">Пример 1: получение блокировки</span><span class="sxs-lookup"><span data-stu-id="87bbf-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="87bbf-116">Эта команда получает блокировку ресурса с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="87bbf-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="87bbf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87bbf-117">PARAMETERS</span></span>

### <span data-ttu-id="87bbf-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87bbf-118">-ApiVersion</span></span>
<span data-ttu-id="87bbf-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87bbf-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="87bbf-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="87bbf-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="87bbf-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="87bbf-121">-AtScope</span></span>
<span data-ttu-id="87bbf-122">Указывает на то, что этот командлет возвращает все блокировки в указанном масштабе или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="87bbf-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="87bbf-123">Если этот параметр не указан, командлет возвращает все блокировки, расположенные выше или ниже области.</span><span class="sxs-lookup"><span data-stu-id="87bbf-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="87bbf-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87bbf-124">-InformationAction</span></span>
<span data-ttu-id="87bbf-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="87bbf-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87bbf-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="87bbf-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87bbf-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="87bbf-127">Continue</span></span>
- <span data-ttu-id="87bbf-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="87bbf-128">Ignore</span></span>
- <span data-ttu-id="87bbf-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="87bbf-129">Inquire</span></span>
- <span data-ttu-id="87bbf-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87bbf-130">SilentlyContinue</span></span>
- <span data-ttu-id="87bbf-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="87bbf-131">Stop</span></span>
- <span data-ttu-id="87bbf-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="87bbf-132">Suspend</span></span>

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

### <span data-ttu-id="87bbf-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87bbf-133">-InformationVariable</span></span>
<span data-ttu-id="87bbf-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="87bbf-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87bbf-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="87bbf-135">-LockId</span></span>
<span data-ttu-id="87bbf-136">Указывает идентификатор блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87bbf-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="87bbf-137">-LockName</span></span>
<span data-ttu-id="87bbf-138">Указывает имя блокировки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87bbf-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="87bbf-139">-Pre</span></span>
<span data-ttu-id="87bbf-140">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="87bbf-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="87bbf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87bbf-141">-ResourceGroupName</span></span>
<span data-ttu-id="87bbf-142">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87bbf-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="87bbf-143">Этот командлет получает блокировки для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87bbf-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="87bbf-144">-ResourceName</span></span>
<span data-ttu-id="87bbf-145">Указывает имя ресурса, к которому применяется эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="87bbf-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="87bbf-146">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="87bbf-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="87bbf-147">-ResourceType</span></span>
<span data-ttu-id="87bbf-148">Указывает тип ресурса, к которому относится эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="87bbf-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="87bbf-149">Этот командлет получает блокировки для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="87bbf-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-150">-Scope</span><span class="sxs-lookup"><span data-stu-id="87bbf-150">-Scope</span></span>
<span data-ttu-id="87bbf-151">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87bbf-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="87bbf-152">Командлет получает блокировки для этой области.</span><span class="sxs-lookup"><span data-stu-id="87bbf-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="87bbf-153">-TenantLevel</span></span>
<span data-ttu-id="87bbf-154">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="87bbf-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87bbf-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bbf-155">-DefaultProfile</span></span>
<span data-ttu-id="87bbf-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87bbf-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87bbf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bbf-157">CommonParameters</span></span>
<span data-ttu-id="87bbf-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87bbf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bbf-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87bbf-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bbf-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87bbf-160">INPUTS</span></span>

## <span data-ttu-id="87bbf-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bbf-161">OUTPUTS</span></span>

### <span data-ttu-id="87bbf-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87bbf-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87bbf-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="87bbf-163">NOTES</span></span>

## <span data-ttu-id="87bbf-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87bbf-164">RELATED LINKS</span></span>

[<span data-ttu-id="87bbf-165">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87bbf-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="87bbf-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87bbf-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="87bbf-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87bbf-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


