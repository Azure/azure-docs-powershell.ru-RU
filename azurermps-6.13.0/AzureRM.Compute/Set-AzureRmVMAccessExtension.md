---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0a2d3ce354a5039db21fdd336f6f2d64efdb56fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568930"
---
# <span data-ttu-id="ac84e-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac84e-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="ac84e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac84e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac84e-103">Добавляет расширение VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac84e-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac84e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac84e-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac84e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac84e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac84e-106">Командлет **Set-AzureRmVMAccessExtension** добавляет для виртуальной машины расширение VMAccess "доступ к виртуальной машине (VMAccess)".</span><span class="sxs-lookup"><span data-stu-id="ac84e-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="ac84e-107">Вы можете использовать расширение VMAccess, чтобы установить временный пароль, и его следует немедленно изменить после входа на компьютер.</span><span class="sxs-lookup"><span data-stu-id="ac84e-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="ac84e-108">Это действие не поддерживается на контроллерах доменов Windows.</span><span class="sxs-lookup"><span data-stu-id="ac84e-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="ac84e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac84e-109">EXAMPLES</span></span>

### <span data-ttu-id="ac84e-110">Пример 1: Добавление расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="ac84e-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="ac84e-111">Эта команда добавляет расширение VMAccess для виртуальной машины с именем VirtualMachine07 в ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ac84e-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="ac84e-112">Команда задает версию обработчика имени и типа для VMAccess.</span><span class="sxs-lookup"><span data-stu-id="ac84e-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="ac84e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac84e-113">PARAMETERS</span></span>

### <span data-ttu-id="ac84e-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="ac84e-114">-Credential</span></span>
<span data-ttu-id="ac84e-115">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="ac84e-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ac84e-116">Если вы вводите имя, отличное от учетной записи текущего локального администратора на виртуальной машине, расширение VMAccess добавит учетную запись локального администратора с этим именем и присвойте указанному паролю учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ac84e-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="ac84e-117">Если локальная учетная запись администратора на виртуальной машине существует, она сбрасывает пароль, а если она отключена, расширение VMAccess включает его.</span><span class="sxs-lookup"><span data-stu-id="ac84e-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="ac84e-118">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ac84e-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ac84e-119">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ac84e-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="ac84e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac84e-120">-DefaultProfile</span></span>
<span data-ttu-id="ac84e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac84e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac84e-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ac84e-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="ac84e-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ac84e-123">-ForceRerun</span></span>
<span data-ttu-id="ac84e-124">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="ac84e-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ac84e-125">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="ac84e-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ac84e-126">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="ac84e-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ac84e-127">-Location</span><span class="sxs-lookup"><span data-stu-id="ac84e-127">-Location</span></span>
<span data-ttu-id="ac84e-128">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac84e-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ac84e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac84e-129">-Name</span></span>
<span data-ttu-id="ac84e-130">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ac84e-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ac84e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac84e-131">-ResourceGroupName</span></span>
<span data-ttu-id="ac84e-132">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac84e-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ac84e-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ac84e-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="ac84e-134">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac84e-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ac84e-135">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="ac84e-135">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="ac84e-136">TypeHandlerVersion должен быть 2,0 или выше, поскольку версия 1 устарела.</span><span class="sxs-lookup"><span data-stu-id="ac84e-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="ac84e-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="ac84e-137">-VMName</span></span>
<span data-ttu-id="ac84e-138">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac84e-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ac84e-139">Этот командлет добавляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac84e-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac84e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac84e-140">-Confirm</span></span>
<span data-ttu-id="ac84e-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac84e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac84e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac84e-142">-WhatIf</span></span>
<span data-ttu-id="ac84e-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac84e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac84e-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac84e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac84e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac84e-145">CommonParameters</span></span>
<span data-ttu-id="ac84e-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac84e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac84e-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac84e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac84e-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac84e-148">INPUTS</span></span>

### <span data-ttu-id="ac84e-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ac84e-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ac84e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ac84e-150">System.String</span></span>

### <span data-ttu-id="ac84e-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac84e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac84e-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac84e-152">OUTPUTS</span></span>

### <span data-ttu-id="ac84e-153">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ac84e-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ac84e-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac84e-154">NOTES</span></span>

## <span data-ttu-id="ac84e-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac84e-155">RELATED LINKS</span></span>

[<span data-ttu-id="ac84e-156">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac84e-156">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="ac84e-157">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac84e-157">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="ac84e-158">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ac84e-158">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="ac84e-159">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ac84e-159">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


