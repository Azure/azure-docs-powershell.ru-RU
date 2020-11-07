---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731238"
---
# <span data-ttu-id="9a8a0-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9a8a0-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="9a8a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8a0-103">Добавляет расширение VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="9a8a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a8a0-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="9a8a0-106">Командлет **Set-AzVMAccessExtension** добавляет для виртуальной машины расширение VMAccess "доступ к виртуальной машине (VMAccess)".</span><span class="sxs-lookup"><span data-stu-id="9a8a0-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="9a8a0-107">Вы можете использовать расширение VMAccess, чтобы установить временный пароль, и его следует немедленно изменить после входа на компьютер.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="9a8a0-108">Это действие не поддерживается на контроллерах доменов Windows.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="9a8a0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="9a8a0-110">Пример 1: Добавление расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="9a8a0-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="9a8a0-111">Эта команда добавляет расширение VMAccess для виртуальной машины с именем VirtualMachine07 в ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="9a8a0-112">Команда задает версию обработчика имени и типа для VMAccess.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="9a8a0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a8a0-113">PARAMETERS</span></span>

### <span data-ttu-id="9a8a0-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="9a8a0-114">-Credential</span></span>
<span data-ttu-id="9a8a0-115">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="9a8a0-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="9a8a0-116">Если вы вводите имя, отличное от учетной записи текущего локального администратора на виртуальной машине, расширение VMAccess добавит учетную запись локального администратора с этим именем и присвойте указанному паролю учетную запись.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="9a8a0-117">Если локальная учетная запись администратора на виртуальной машине существует, она сбрасывает пароль, а если она отключена, расширение VMAccess включает его.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="9a8a0-118">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="9a8a0-119">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9a8a0-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="9a8a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8a0-120">-DefaultProfile</span></span>
<span data-ttu-id="9a8a0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a8a0-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9a8a0-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="9a8a0-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9a8a0-123">-ForceRerun</span></span>
<span data-ttu-id="9a8a0-124">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="9a8a0-125">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="9a8a0-126">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9a8a0-127">-Location</span><span class="sxs-lookup"><span data-stu-id="9a8a0-127">-Location</span></span>
<span data-ttu-id="9a8a0-128">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9a8a0-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a8a0-129">-Name</span></span>
<span data-ttu-id="9a8a0-130">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9a8a0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8a0-131">-ResourceGroupName</span></span>
<span data-ttu-id="9a8a0-132">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9a8a0-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9a8a0-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="9a8a0-134">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9a8a0-135">Чтобы получить версию, выполните командлет Get-AzVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="9a8a0-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="9a8a0-136">TypeHandlerVersion должен быть 2,0 или выше, поскольку версия 1 устарела.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="9a8a0-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="9a8a0-137">-VMName</span></span>
<span data-ttu-id="9a8a0-138">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9a8a0-139">Этот командлет добавляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9a8a0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a8a0-140">-Confirm</span></span>
<span data-ttu-id="9a8a0-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8a0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8a0-142">-WhatIf</span></span>
<span data-ttu-id="9a8a0-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8a0-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8a0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8a0-145">CommonParameters</span></span>
<span data-ttu-id="9a8a0-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a8a0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8a0-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8a0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8a0-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a8a0-148">INPUTS</span></span>

### <span data-ttu-id="9a8a0-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9a8a0-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="9a8a0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9a8a0-150">System.String</span></span>

### <span data-ttu-id="9a8a0-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a8a0-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a8a0-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8a0-152">OUTPUTS</span></span>

### <span data-ttu-id="9a8a0-153">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9a8a0-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9a8a0-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a8a0-154">NOTES</span></span>

## <span data-ttu-id="9a8a0-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a8a0-155">RELATED LINKS</span></span>

[<span data-ttu-id="9a8a0-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9a8a0-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="9a8a0-157">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9a8a0-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="9a8a0-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9a8a0-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="9a8a0-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9a8a0-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


