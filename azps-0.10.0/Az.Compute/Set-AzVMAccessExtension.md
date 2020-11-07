---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911352"
---
# <span data-ttu-id="eb7f8-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eb7f8-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="eb7f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7f8-103">Добавляет расширение VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="eb7f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb7f8-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb7f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7f8-106">Командлет **Set-AzVMAccessExtension** добавляет для виртуальной машины расширение VMAccess "доступ к виртуальной машине (VMAccess)".</span><span class="sxs-lookup"><span data-stu-id="eb7f8-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="eb7f8-107">Вы можете использовать расширение VMAccess, чтобы установить временный пароль, и его следует немедленно изменить после входа на компьютер.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="eb7f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb7f8-108">EXAMPLES</span></span>

### <span data-ttu-id="eb7f8-109">Пример 1: Добавление расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="eb7f8-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="eb7f8-110">Эта команда добавляет расширение VMAccess для виртуальной машины с именем VirtualMachine07 в ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="eb7f8-111">Команда задает версию обработчика имени и типа для VMAccess.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="eb7f8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb7f8-112">PARAMETERS</span></span>

### <span data-ttu-id="eb7f8-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="eb7f8-113">-Credential</span></span>
<span data-ttu-id="eb7f8-114">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="eb7f8-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="eb7f8-115">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="eb7f8-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="eb7f8-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7f8-117">-DefaultProfile</span></span>
<span data-ttu-id="eb7f8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="eb7f8-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="eb7f8-120">-ForceRerun</span></span>
<span data-ttu-id="eb7f8-121">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="eb7f8-122">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="eb7f8-123">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="eb7f8-124">-Location</span></span>
<span data-ttu-id="eb7f8-125">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb7f8-126">-Name</span></span>
<span data-ttu-id="eb7f8-127">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-127">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb7f8-129">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="eb7f8-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="eb7f8-131">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="eb7f8-132">Чтобы получить версию, выполните командлет Get-AzVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="eb7f8-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb7f8-133">-VMName</span></span>
<span data-ttu-id="eb7f8-134">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="eb7f8-135">Этот командлет добавляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb7f8-136">-Confirm</span></span>
<span data-ttu-id="eb7f8-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7f8-138">-WhatIf</span></span>
<span data-ttu-id="eb7f8-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="eb7f8-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7f8-141">CommonParameters</span></span>
<span data-ttu-id="eb7f8-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7f8-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7f8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7f8-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb7f8-144">INPUTS</span></span>

### <span data-ttu-id="eb7f8-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb7f8-145">None</span></span>
<span data-ttu-id="eb7f8-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb7f8-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb7f8-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7f8-147">OUTPUTS</span></span>

### <span data-ttu-id="eb7f8-148">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb7f8-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eb7f8-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb7f8-149">NOTES</span></span>

## <span data-ttu-id="eb7f8-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb7f8-150">RELATED LINKS</span></span>

[<span data-ttu-id="eb7f8-151">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eb7f8-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="eb7f8-152">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eb7f8-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="eb7f8-153">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="eb7f8-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="eb7f8-154">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="eb7f8-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


