---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914153"
---
# <span data-ttu-id="f169e-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f169e-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="f169e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f169e-102">SYNOPSIS</span></span>
<span data-ttu-id="f169e-103">Добавляет расширение VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f169e-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f169e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f169e-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f169e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f169e-105">DESCRIPTION</span></span>
<span data-ttu-id="f169e-106">Командлет **Set-AzureRmVMAccessExtension** добавляет для виртуальной машины расширение VMAccess "доступ к виртуальной машине (VMAccess)".</span><span class="sxs-lookup"><span data-stu-id="f169e-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="f169e-107">Вы можете использовать расширение VMAccess, чтобы установить временный пароль, и его следует немедленно изменить после входа на компьютер.</span><span class="sxs-lookup"><span data-stu-id="f169e-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="f169e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f169e-108">EXAMPLES</span></span>

### <span data-ttu-id="f169e-109">Пример 1: Добавление расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="f169e-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="f169e-110">Эта команда добавляет расширение VMAccess для виртуальной машины с именем VirtualMachine07 в ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f169e-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="f169e-111">Команда задает версию обработчика имени и типа для VMAccess.</span><span class="sxs-lookup"><span data-stu-id="f169e-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="f169e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f169e-112">PARAMETERS</span></span>

### <span data-ttu-id="f169e-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="f169e-113">-Credential</span></span>
<span data-ttu-id="f169e-114">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="f169e-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f169e-115">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f169e-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f169e-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f169e-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="f169e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f169e-117">-DefaultProfile</span></span>
<span data-ttu-id="f169e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f169e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f169e-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f169e-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="f169e-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f169e-120">-ForceRerun</span></span>
<span data-ttu-id="f169e-121">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="f169e-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f169e-122">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="f169e-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f169e-123">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="f169e-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f169e-124">-Location</span><span class="sxs-lookup"><span data-stu-id="f169e-124">-Location</span></span>
<span data-ttu-id="f169e-125">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f169e-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f169e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f169e-126">-Name</span></span>
<span data-ttu-id="f169e-127">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f169e-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f169e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f169e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f169e-129">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f169e-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f169e-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f169e-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="f169e-131">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f169e-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f169e-132">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="f169e-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="f169e-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="f169e-133">-VMName</span></span>
<span data-ttu-id="f169e-134">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f169e-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f169e-135">Этот командлет добавляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f169e-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f169e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f169e-136">-Confirm</span></span>
<span data-ttu-id="f169e-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f169e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f169e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f169e-138">-WhatIf</span></span>
<span data-ttu-id="f169e-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f169e-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f169e-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f169e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f169e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f169e-141">CommonParameters</span></span>
<span data-ttu-id="f169e-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f169e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f169e-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f169e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f169e-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f169e-144">INPUTS</span></span>

### <span data-ttu-id="f169e-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="f169e-145">None</span></span>
<span data-ttu-id="f169e-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f169e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f169e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f169e-147">OUTPUTS</span></span>

### <span data-ttu-id="f169e-148">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f169e-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f169e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="f169e-149">NOTES</span></span>

## <span data-ttu-id="f169e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f169e-150">RELATED LINKS</span></span>

[<span data-ttu-id="f169e-151">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f169e-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f169e-152">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f169e-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f169e-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f169e-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="f169e-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f169e-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


