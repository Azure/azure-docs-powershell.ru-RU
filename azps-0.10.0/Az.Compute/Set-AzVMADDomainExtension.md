---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 99dd311adf976e100282da92db6a3147880feefb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911353"
---
# <span data-ttu-id="5faa1-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5faa1-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="5faa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5faa1-102">SYNOPSIS</span></span>
<span data-ttu-id="5faa1-103">Добавляет расширение доменных служб Active Directory на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5faa1-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="5faa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5faa1-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5faa1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5faa1-105">DESCRIPTION</span></span>
<span data-ttu-id="5faa1-106">Командлет **Set-AzVMADDomainExtension** добавляет расширение виртуальной машины Azure Active Directory (AD) к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5faa1-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="5faa1-107">Это расширение позволяет присоединиться к домену с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5faa1-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="5faa1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5faa1-108">EXAMPLES</span></span>

## <span data-ttu-id="5faa1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5faa1-109">PARAMETERS</span></span>

### <span data-ttu-id="5faa1-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="5faa1-110">-Credential</span></span>
<span data-ttu-id="5faa1-111">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5faa1-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5faa1-112">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5faa1-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5faa1-113">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5faa1-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="5faa1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faa1-114">-DefaultProfile</span></span>
<span data-ttu-id="5faa1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5faa1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5faa1-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5faa1-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5faa1-117">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="5faa1-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="5faa1-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="5faa1-118">-DomainName</span></span>
<span data-ttu-id="5faa1-119">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="5faa1-119">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5faa1-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5faa1-120">-ForceRerun</span></span>
<span data-ttu-id="5faa1-121">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="5faa1-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5faa1-122">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="5faa1-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5faa1-123">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="5faa1-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5faa1-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="5faa1-124">-JoinOption</span></span>
<span data-ttu-id="5faa1-125">Задает параметр присоединения.</span><span class="sxs-lookup"><span data-stu-id="5faa1-125">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5faa1-126">-Location</span><span class="sxs-lookup"><span data-stu-id="5faa1-126">-Location</span></span>
<span data-ttu-id="5faa1-127">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5faa1-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5faa1-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5faa1-128">-Name</span></span>
<span data-ttu-id="5faa1-129">Указывает имя добавляемого расширения домена.</span><span class="sxs-lookup"><span data-stu-id="5faa1-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="5faa1-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="5faa1-130">-OUPath</span></span>
<span data-ttu-id="5faa1-131">Определяет организационное подразделение (OU) для учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="5faa1-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="5faa1-132">Введите полное различающееся имя подразделения в кавычки.</span><span class="sxs-lookup"><span data-stu-id="5faa1-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="5faa1-133">Значением по умолчанию является подразделение по умолчанию для объектов компьютеров в домене.</span><span class="sxs-lookup"><span data-stu-id="5faa1-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="5faa1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5faa1-134">-ResourceGroupName</span></span>
<span data-ttu-id="5faa1-135">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5faa1-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5faa1-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="5faa1-136">-Restart</span></span>
<span data-ttu-id="5faa1-137">Указывает на то, что этот командлет перезапускает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5faa1-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="5faa1-138">Для вступления изменений в силу часто требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="5faa1-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="5faa1-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5faa1-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="5faa1-140">Указывает версию расширения домена.</span><span class="sxs-lookup"><span data-stu-id="5faa1-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="5faa1-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="5faa1-141">-VMName</span></span>
<span data-ttu-id="5faa1-142">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5faa1-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5faa1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5faa1-143">-Confirm</span></span>
<span data-ttu-id="5faa1-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5faa1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5faa1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5faa1-145">-WhatIf</span></span>
<span data-ttu-id="5faa1-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5faa1-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5faa1-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5faa1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5faa1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faa1-148">CommonParameters</span></span>
<span data-ttu-id="5faa1-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5faa1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faa1-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5faa1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faa1-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5faa1-151">INPUTS</span></span>

### <span data-ttu-id="5faa1-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="5faa1-152">None</span></span>
<span data-ttu-id="5faa1-153">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5faa1-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5faa1-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5faa1-154">OUTPUTS</span></span>

### <span data-ttu-id="5faa1-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5faa1-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5faa1-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="5faa1-156">NOTES</span></span>

## <span data-ttu-id="5faa1-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5faa1-157">RELATED LINKS</span></span>

[<span data-ttu-id="5faa1-158">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5faa1-158">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
