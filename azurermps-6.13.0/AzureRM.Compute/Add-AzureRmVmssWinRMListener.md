---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 23da9524d2641f390fcd29a62fd469d34cf05de3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565872"
---
# <span data-ttu-id="73a6b-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="73a6b-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="73a6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="73a6b-103">Добавляет прослушиватель WinRM в VMSS.</span><span class="sxs-lookup"><span data-stu-id="73a6b-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73a6b-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73a6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="73a6b-106">Командлет **Add-AzureRmVmssWinRMListener** добавляет прослушиватель удаленного управления Windows (WinRM) в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="73a6b-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="73a6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="73a6b-108">Пример 1: Добавление прослушивателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="73a6b-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="73a6b-109">В этом примере в VMSS добавляется прослушиватель WinRM.</span><span class="sxs-lookup"><span data-stu-id="73a6b-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="73a6b-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="73a6b-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="73a6b-111">Вторая команда добавляет прослушиватель HTTP протокола WinRM с сертификатом по указанному URL-адресу в VMSS.</span><span class="sxs-lookup"><span data-stu-id="73a6b-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="73a6b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73a6b-112">PARAMETERS</span></span>

### <span data-ttu-id="73a6b-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="73a6b-113">-CertificateUrl</span></span>
<span data-ttu-id="73a6b-114">Указывает ссылку (URL-адрес) сертификата, с помощью которого будут подготавливаться новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="73a6b-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a6b-115">-DefaultProfile</span></span>
<span data-ttu-id="73a6b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73a6b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a6b-117">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="73a6b-117">-Protocol</span></span>
<span data-ttu-id="73a6b-118">Задает протокол для прослушивателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="73a6b-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="73a6b-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="73a6b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="73a6b-120">Через</span><span class="sxs-lookup"><span data-stu-id="73a6b-120">Http</span></span>
- <span data-ttu-id="73a6b-121">Протокол</span><span class="sxs-lookup"><span data-stu-id="73a6b-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a6b-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73a6b-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="73a6b-123">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="73a6b-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="73a6b-124">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="73a6b-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73a6b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a6b-125">-Confirm</span></span>
<span data-ttu-id="73a6b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73a6b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a6b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a6b-127">-WhatIf</span></span>
<span data-ttu-id="73a6b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73a6b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73a6b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73a6b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a6b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a6b-130">CommonParameters</span></span>
<span data-ttu-id="73a6b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73a6b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a6b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a6b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a6b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73a6b-133">INPUTS</span></span>

### <span data-ttu-id="73a6b-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73a6b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="73a6b-135">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ProtocolTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="73a6b-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="73a6b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="73a6b-136">System.String</span></span>

## <span data-ttu-id="73a6b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73a6b-137">OUTPUTS</span></span>

### <span data-ttu-id="73a6b-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73a6b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="73a6b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="73a6b-139">NOTES</span></span>

## <span data-ttu-id="73a6b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73a6b-140">RELATED LINKS</span></span>

[<span data-ttu-id="73a6b-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73a6b-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


