---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568934"
---
# <span data-ttu-id="09545-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="09545-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="09545-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09545-102">SYNOPSIS</span></span>
<span data-ttu-id="09545-103">Добавляет расширение доменных служб Active Directory на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="09545-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09545-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09545-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09545-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09545-105">DESCRIPTION</span></span>
<span data-ttu-id="09545-106">Командлет **Set-AzureRmVMADDomainExtension** добавляет расширение виртуальной машины Azure Active Directory (AD) к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="09545-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="09545-107">Это расширение позволяет присоединиться к домену с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09545-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="09545-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09545-108">EXAMPLES</span></span>

## <span data-ttu-id="09545-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09545-109">PARAMETERS</span></span>

### <span data-ttu-id="09545-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="09545-110">-Credential</span></span>
<span data-ttu-id="09545-111">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="09545-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="09545-112">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="09545-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="09545-113">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="09545-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="09545-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09545-114">-DefaultProfile</span></span>
<span data-ttu-id="09545-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09545-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09545-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="09545-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="09545-117">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="09545-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="09545-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="09545-118">-DomainName</span></span>
<span data-ttu-id="09545-119">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="09545-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="09545-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="09545-120">-ForceRerun</span></span>
<span data-ttu-id="09545-121">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="09545-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="09545-122">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="09545-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="09545-123">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="09545-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="09545-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="09545-124">-JoinOption</span></span>
<span data-ttu-id="09545-125">Задает параметр присоединения.</span><span class="sxs-lookup"><span data-stu-id="09545-125">Specifies the join option.</span></span> <span data-ttu-id="09545-126">Параметры объединения см [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="09545-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="09545-127">-Location</span><span class="sxs-lookup"><span data-stu-id="09545-127">-Location</span></span>
<span data-ttu-id="09545-128">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09545-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="09545-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09545-129">-Name</span></span>
<span data-ttu-id="09545-130">Указывает имя добавляемого расширения домена.</span><span class="sxs-lookup"><span data-stu-id="09545-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="09545-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="09545-131">-OUPath</span></span>
<span data-ttu-id="09545-132">Определяет организационное подразделение (OU) для учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="09545-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="09545-133">Введите полное различающееся имя подразделения в кавычки.</span><span class="sxs-lookup"><span data-stu-id="09545-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="09545-134">Значением по умолчанию является подразделение по умолчанию для объектов компьютеров в домене.</span><span class="sxs-lookup"><span data-stu-id="09545-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="09545-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09545-135">-ResourceGroupName</span></span>
<span data-ttu-id="09545-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09545-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="09545-137">-Restart</span><span class="sxs-lookup"><span data-stu-id="09545-137">-Restart</span></span>
<span data-ttu-id="09545-138">Указывает на то, что этот командлет перезапускает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="09545-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="09545-139">Для вступления изменений в силу часто требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="09545-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="09545-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="09545-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="09545-141">Указывает версию расширения домена.</span><span class="sxs-lookup"><span data-stu-id="09545-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="09545-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="09545-142">-VMName</span></span>
<span data-ttu-id="09545-143">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09545-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="09545-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09545-144">-Confirm</span></span>
<span data-ttu-id="09545-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09545-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09545-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09545-146">-WhatIf</span></span>
<span data-ttu-id="09545-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09545-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09545-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09545-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09545-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09545-149">CommonParameters</span></span>
<span data-ttu-id="09545-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09545-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09545-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09545-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09545-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09545-152">INPUTS</span></span>

### <span data-ttu-id="09545-153">System. String</span><span class="sxs-lookup"><span data-stu-id="09545-153">System.String</span></span>

### <span data-ttu-id="09545-154">System. Nullable "1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09545-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="09545-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="09545-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="09545-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="09545-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="09545-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09545-157">OUTPUTS</span></span>

### <span data-ttu-id="09545-158">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="09545-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="09545-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="09545-159">NOTES</span></span>

## <span data-ttu-id="09545-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09545-160">RELATED LINKS</span></span>

[<span data-ttu-id="09545-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="09545-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
