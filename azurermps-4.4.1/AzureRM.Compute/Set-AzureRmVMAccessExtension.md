---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557823"
---
# <span data-ttu-id="bcc84-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bcc84-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="bcc84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcc84-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc84-103">Добавляет расширение VMAccess на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bcc84-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcc84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcc84-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc84-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcc84-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc84-106">Командлет **Set-AzureRmVMAccessExtension** добавляет расширение виртуальной машины для доступа к виртуальной машине (VMAccess) к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bcc84-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="bcc84-107">VMAccess может сбросить имя пользователя и пароль для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="bcc84-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcc84-108">EXAMPLES</span></span>

### <span data-ttu-id="bcc84-109">Пример 1: Добавление расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="bcc84-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="bcc84-110">Эта команда добавляет расширение VMAccess для виртуальной машины с именем VirtualMachine07 в ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bcc84-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="bcc84-111">Команда задает версию обработчика имени и типа для VMAccess.</span><span class="sxs-lookup"><span data-stu-id="bcc84-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="bcc84-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcc84-112">PARAMETERS</span></span>

### <span data-ttu-id="bcc84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc84-113">-DefaultProfile</span></span>
<span data-ttu-id="bcc84-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcc84-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bcc84-115">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="bcc84-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bcc84-116">-ForceRerun</span></span>
<span data-ttu-id="bcc84-117">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="bcc84-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="bcc84-118">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="bcc84-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="bcc84-119">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="bcc84-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="bcc84-120">-Location</span><span class="sxs-lookup"><span data-stu-id="bcc84-120">-Location</span></span>
<span data-ttu-id="bcc84-121">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-121">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="bcc84-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcc84-122">-Name</span></span>
<span data-ttu-id="bcc84-123">Указывает имя расширения, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bcc84-123">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bcc84-124">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="bcc84-124">-Password</span></span>
<span data-ttu-id="bcc84-125">Указывает новый пароль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-125">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="bcc84-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc84-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcc84-127">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bcc84-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bcc84-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="bcc84-129">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="bcc84-130">Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="bcc84-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="bcc84-131">-UserName</span><span class="sxs-lookup"><span data-stu-id="bcc84-131">-UserName</span></span>
<span data-ttu-id="bcc84-132">Указывает новое имя пользователя для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-132">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="bcc84-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="bcc84-133">-VMName</span></span>
<span data-ttu-id="bcc84-134">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcc84-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bcc84-135">Этот командлет добавляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bcc84-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="bcc84-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcc84-136">-Confirm</span></span>
<span data-ttu-id="bcc84-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcc84-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc84-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc84-138">-WhatIf</span></span>
<span data-ttu-id="bcc84-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcc84-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bcc84-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcc84-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc84-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc84-141">CommonParameters</span></span>
<span data-ttu-id="bcc84-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcc84-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc84-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc84-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc84-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcc84-144">INPUTS</span></span>

## <span data-ttu-id="bcc84-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcc84-145">OUTPUTS</span></span>

## <span data-ttu-id="bcc84-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcc84-146">NOTES</span></span>

## <span data-ttu-id="bcc84-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcc84-147">RELATED LINKS</span></span>

[<span data-ttu-id="bcc84-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bcc84-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="bcc84-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bcc84-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="bcc84-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="bcc84-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="bcc84-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="bcc84-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


