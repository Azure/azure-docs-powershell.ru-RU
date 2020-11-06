---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557508"
---
# <span data-ttu-id="a9636-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a9636-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="a9636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9636-102">SYNOPSIS</span></span>
<span data-ttu-id="a9636-103">Добавляет расширение доменных служб Active Directory на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a9636-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9636-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9636-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9636-105">DESCRIPTION</span></span>
<span data-ttu-id="a9636-106">Командлет **Set-AzureRmVMADDomainExtension** добавляет расширение виртуальной машины Azure Active Directory (AD) к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a9636-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="a9636-107">Это расширение позволяет присоединиться к домену с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9636-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="a9636-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9636-108">EXAMPLES</span></span>

## <span data-ttu-id="a9636-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9636-109">PARAMETERS</span></span>

### <span data-ttu-id="a9636-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="a9636-110">-Credential</span></span>
<span data-ttu-id="a9636-111">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="a9636-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="a9636-112">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="a9636-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a9636-113">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a9636-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="a9636-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a9636-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a9636-115">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="a9636-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="a9636-116">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="a9636-116">-DomainName</span></span>
<span data-ttu-id="a9636-117">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="a9636-117">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="a9636-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a9636-118">-ForceRerun</span></span>
<span data-ttu-id="a9636-119">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="a9636-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a9636-120">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="a9636-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="a9636-121">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="a9636-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a9636-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="a9636-122">-JoinOption</span></span>
<span data-ttu-id="a9636-123">Задает параметр присоединения.</span><span class="sxs-lookup"><span data-stu-id="a9636-123">Specifies the join option.</span></span>

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

### <span data-ttu-id="a9636-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a9636-124">-Location</span></span>
<span data-ttu-id="a9636-125">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9636-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a9636-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9636-126">-Name</span></span>
<span data-ttu-id="a9636-127">Указывает имя добавляемого расширения домена.</span><span class="sxs-lookup"><span data-stu-id="a9636-127">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="a9636-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="a9636-128">-OUPath</span></span>
<span data-ttu-id="a9636-129">Определяет организационное подразделение (OU) для учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="a9636-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="a9636-130">Введите полное различающееся имя подразделения в кавычки.</span><span class="sxs-lookup"><span data-stu-id="a9636-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="a9636-131">Значением по умолчанию является подразделение по умолчанию для объектов компьютеров в домене.</span><span class="sxs-lookup"><span data-stu-id="a9636-131">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="a9636-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9636-132">-ResourceGroupName</span></span>
<span data-ttu-id="a9636-133">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9636-133">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a9636-134">-Restart</span><span class="sxs-lookup"><span data-stu-id="a9636-134">-Restart</span></span>
<span data-ttu-id="a9636-135">Указывает на то, что этот командлет перезапускает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a9636-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="a9636-136">Для вступления изменений в силу часто требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="a9636-136">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="a9636-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a9636-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="a9636-138">Указывает версию расширения домена.</span><span class="sxs-lookup"><span data-stu-id="a9636-138">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="a9636-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="a9636-139">-VMName</span></span>
<span data-ttu-id="a9636-140">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9636-140">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a9636-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9636-141">-Confirm</span></span>
<span data-ttu-id="a9636-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9636-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9636-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9636-143">-WhatIf</span></span>
<span data-ttu-id="a9636-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9636-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a9636-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9636-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9636-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9636-146">CommonParameters</span></span>
<span data-ttu-id="a9636-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9636-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9636-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9636-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9636-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9636-149">INPUTS</span></span>

### <span data-ttu-id="a9636-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9636-150">None</span></span>
<span data-ttu-id="a9636-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a9636-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9636-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9636-152">OUTPUTS</span></span>

## <span data-ttu-id="a9636-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9636-153">NOTES</span></span>

## <span data-ttu-id="a9636-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9636-154">RELATED LINKS</span></span>

[<span data-ttu-id="a9636-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a9636-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
