---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078455"
---
# <span data-ttu-id="598ce-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="598ce-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="598ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="598ce-102">SYNOPSIS</span></span>
<span data-ttu-id="598ce-103">Добавляет прослушиватель WinRM в VMSS.</span><span class="sxs-lookup"><span data-stu-id="598ce-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="598ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="598ce-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="598ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="598ce-105">DESCRIPTION</span></span>
<span data-ttu-id="598ce-106">Командлет **Add-AzVmssWinRMListener** добавляет прослушиватель удаленного управления Windows (WinRM) в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="598ce-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="598ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="598ce-107">EXAMPLES</span></span>

### <span data-ttu-id="598ce-108">Пример 1: Добавление прослушивателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="598ce-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="598ce-109">В этом примере в VMSS добавляется прослушиватель WinRM.</span><span class="sxs-lookup"><span data-stu-id="598ce-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="598ce-110">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="598ce-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="598ce-111">Вторая команда добавляет прослушиватель HTTP протокола WinRM с сертификатом по указанному URL-адресу в VMSS.</span><span class="sxs-lookup"><span data-stu-id="598ce-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="598ce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="598ce-112">PARAMETERS</span></span>

### <span data-ttu-id="598ce-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="598ce-113">-CertificateUrl</span></span>
<span data-ttu-id="598ce-114">Указывает ссылку (URL-адрес) сертификата, с помощью которого будут подготавливаться новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="598ce-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="598ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598ce-115">-DefaultProfile</span></span>
<span data-ttu-id="598ce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="598ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="598ce-117">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="598ce-117">-Protocol</span></span>
<span data-ttu-id="598ce-118">Задает протокол для прослушивателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="598ce-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="598ce-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="598ce-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="598ce-120">Через</span><span class="sxs-lookup"><span data-stu-id="598ce-120">Http</span></span>
- <span data-ttu-id="598ce-121">Протокол</span><span class="sxs-lookup"><span data-stu-id="598ce-121">Https</span></span>

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

### <span data-ttu-id="598ce-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="598ce-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="598ce-123">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="598ce-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="598ce-124">Для создания объекта можно использовать командлет New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="598ce-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="598ce-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="598ce-125">-Confirm</span></span>
<span data-ttu-id="598ce-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="598ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598ce-127">-WhatIf</span></span>
<span data-ttu-id="598ce-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="598ce-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="598ce-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="598ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598ce-130">CommonParameters</span></span>
<span data-ttu-id="598ce-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="598ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598ce-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="598ce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598ce-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="598ce-133">INPUTS</span></span>

### <span data-ttu-id="598ce-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="598ce-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="598ce-135">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ProtocolTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="598ce-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="598ce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="598ce-136">System.String</span></span>

## <span data-ttu-id="598ce-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="598ce-137">OUTPUTS</span></span>

### <span data-ttu-id="598ce-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="598ce-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="598ce-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="598ce-139">NOTES</span></span>

## <span data-ttu-id="598ce-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="598ce-140">RELATED LINKS</span></span>

[<span data-ttu-id="598ce-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="598ce-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


