---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509045"
---
# <span data-ttu-id="f0a87-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f0a87-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="f0a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a87-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a87-103">Добавляет расширение домена AD на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0a87-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="f0a87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0a87-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a87-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0a87-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a87-106">Cmdlet **Set-AzVMADDomainExtension** добавляет расширение виртуальной машины домена Azure Active Directory (AD) на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0a87-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="f0a87-107">Это расширение позволяет виртуальной машине присоединиться к домену.</span><span class="sxs-lookup"><span data-stu-id="f0a87-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="f0a87-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0a87-108">EXAMPLES</span></span>

## <span data-ttu-id="f0a87-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0a87-109">PARAMETERS</span></span>

### <span data-ttu-id="f0a87-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="f0a87-110">-Credential</span></span>
<span data-ttu-id="f0a87-111">Указывает имя пользователя и пароль виртуальной машины в качестве **объекта PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="f0a87-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f0a87-112">Для получения учетных данных используйте Get-Credential управления.</span><span class="sxs-lookup"><span data-stu-id="f0a87-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f0a87-113">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f0a87-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a87-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a87-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0a87-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0a87-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f0a87-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f0a87-117">Указывает на то, что этот cmdlet отключает автоматическое обновление незначительных версий расширения.</span><span class="sxs-lookup"><span data-stu-id="f0a87-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="f0a87-118">-DomainName</span></span>
<span data-ttu-id="f0a87-119">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="f0a87-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f0a87-120">-ForceRerun</span></span>
<span data-ttu-id="f0a87-121">Указывает на то, что этот cmdlet приостановит повторение одной и той же конфигурации расширения на виртуальной машине, не устраив и повторно установив расширение.</span><span class="sxs-lookup"><span data-stu-id="f0a87-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f0a87-122">Значение может быть любой строкой, которая отличается от текущей.</span><span class="sxs-lookup"><span data-stu-id="f0a87-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="f0a87-123">Если параметр forceUpdateTag не изменился, обработник по-прежнему применяет обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="f0a87-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="f0a87-124">-JoinOption</span></span>
<span data-ttu-id="f0a87-125">Определяет параметры присоединиться.</span><span class="sxs-lookup"><span data-stu-id="f0a87-125">Specifies the join option.</span></span> <span data-ttu-id="f0a87-126">Параметры присоединиться [см. в fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="f0a87-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f0a87-127">-Location</span></span>
<span data-ttu-id="f0a87-128">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a87-128">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f0a87-129">-Name</span></span>
<span data-ttu-id="f0a87-130">Указывает имя добавляемого расширения домена.</span><span class="sxs-lookup"><span data-stu-id="f0a87-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0a87-131">-NoWait</span></span>
<span data-ttu-id="f0a87-132">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="f0a87-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f0a87-133">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="f0a87-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f0a87-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="f0a87-134">-OUPath</span></span>
<span data-ttu-id="f0a87-135">Определяет подразделение для учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="f0a87-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="f0a87-136">Введите полное различается имя ОО в кавычках.</span><span class="sxs-lookup"><span data-stu-id="f0a87-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="f0a87-137">Значением по умолчанию является стандартный OU для машинных объектов в домене.</span><span class="sxs-lookup"><span data-stu-id="f0a87-137">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a87-138">-ResourceGroupName</span></span>
<span data-ttu-id="f0a87-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0a87-139">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-140">-Перезапустить</span><span class="sxs-lookup"><span data-stu-id="f0a87-140">-Restart</span></span>
<span data-ttu-id="f0a87-141">Указывает на то, что этот cmdlet перезапустит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0a87-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="f0a87-142">Для этого часто требуется перезапуск.</span><span class="sxs-lookup"><span data-stu-id="f0a87-142">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f0a87-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="f0a87-144">Определяет версию расширения домена.</span><span class="sxs-lookup"><span data-stu-id="f0a87-144">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0a87-145">-VMName</span></span>
<span data-ttu-id="f0a87-146">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0a87-146">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0a87-147">-Confirm</span></span>
<span data-ttu-id="f0a87-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0a87-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a87-149">-WhatIf</span></span>
<span data-ttu-id="f0a87-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0a87-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a87-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0a87-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a87-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a87-152">CommonParameters</span></span>
<span data-ttu-id="f0a87-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a87-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a87-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0a87-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a87-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0a87-155">INPUTS</span></span>

### <span data-ttu-id="f0a87-156">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a87-156">System.String</span></span>

### <span data-ttu-id="f0a87-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0a87-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0a87-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="f0a87-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="f0a87-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0a87-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0a87-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0a87-160">OUTPUTS</span></span>

### <span data-ttu-id="f0a87-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0a87-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f0a87-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0a87-162">NOTES</span></span>

## <span data-ttu-id="f0a87-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0a87-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0a87-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f0a87-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
