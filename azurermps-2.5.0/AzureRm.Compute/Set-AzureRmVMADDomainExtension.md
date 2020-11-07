---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 140f1ccdedd6f3b3402601a8a844092bf3d7ab0e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914909"
---
# <span data-ttu-id="5590e-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5590e-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="5590e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5590e-102">SYNOPSIS</span></span>
<span data-ttu-id="5590e-103">Добавляет расширение доменных служб Active Directory на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5590e-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5590e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5590e-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5590e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5590e-105">DESCRIPTION</span></span>
<span data-ttu-id="5590e-106">Командлет **Set-AzureRmVMADDomainExtension** добавляет расширение виртуальной машины Azure Active Directory (AD) к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5590e-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="5590e-107">Это расширение позволяет присоединиться к домену с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5590e-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="5590e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5590e-108">EXAMPLES</span></span>

## <span data-ttu-id="5590e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5590e-109">PARAMETERS</span></span>

### <span data-ttu-id="5590e-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="5590e-110">-Credential</span></span>
<span data-ttu-id="5590e-111">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5590e-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5590e-112">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5590e-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5590e-113">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5590e-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="5590e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5590e-114">-DefaultProfile</span></span>
<span data-ttu-id="5590e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5590e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5590e-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5590e-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5590e-117">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="5590e-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="5590e-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="5590e-118">-DomainName</span></span>
<span data-ttu-id="5590e-119">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="5590e-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="5590e-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5590e-120">-ForceRerun</span></span>
<span data-ttu-id="5590e-121">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="5590e-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5590e-122">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="5590e-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5590e-123">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="5590e-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5590e-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="5590e-124">-JoinOption</span></span>
<span data-ttu-id="5590e-125">Задает параметр присоединения.</span><span class="sxs-lookup"><span data-stu-id="5590e-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="5590e-126">-Location</span><span class="sxs-lookup"><span data-stu-id="5590e-126">-Location</span></span>
<span data-ttu-id="5590e-127">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5590e-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5590e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5590e-128">-Name</span></span>
<span data-ttu-id="5590e-129">Указывает имя добавляемого расширения домена.</span><span class="sxs-lookup"><span data-stu-id="5590e-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="5590e-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="5590e-130">-OUPath</span></span>
<span data-ttu-id="5590e-131">Определяет организационное подразделение (OU) для учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="5590e-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="5590e-132">Введите полное различающееся имя подразделения в кавычки.</span><span class="sxs-lookup"><span data-stu-id="5590e-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="5590e-133">Значением по умолчанию является подразделение по умолчанию для объектов компьютеров в домене.</span><span class="sxs-lookup"><span data-stu-id="5590e-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="5590e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5590e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5590e-135">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5590e-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5590e-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="5590e-136">-Restart</span></span>
<span data-ttu-id="5590e-137">Указывает на то, что этот командлет перезапускает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5590e-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="5590e-138">Для вступления изменений в силу часто требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="5590e-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="5590e-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5590e-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="5590e-140">Указывает версию расширения домена.</span><span class="sxs-lookup"><span data-stu-id="5590e-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="5590e-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="5590e-141">-VMName</span></span>
<span data-ttu-id="5590e-142">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5590e-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5590e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5590e-143">-Confirm</span></span>
<span data-ttu-id="5590e-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5590e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5590e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5590e-145">-WhatIf</span></span>
<span data-ttu-id="5590e-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5590e-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5590e-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5590e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5590e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5590e-148">CommonParameters</span></span>
<span data-ttu-id="5590e-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5590e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5590e-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5590e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5590e-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5590e-151">INPUTS</span></span>

### <span data-ttu-id="5590e-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="5590e-152">None</span></span>
<span data-ttu-id="5590e-153">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5590e-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5590e-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5590e-154">OUTPUTS</span></span>

### <span data-ttu-id="5590e-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5590e-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5590e-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="5590e-156">NOTES</span></span>

## <span data-ttu-id="5590e-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5590e-157">RELATED LINKS</span></span>

[<span data-ttu-id="5590e-158">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5590e-158">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
