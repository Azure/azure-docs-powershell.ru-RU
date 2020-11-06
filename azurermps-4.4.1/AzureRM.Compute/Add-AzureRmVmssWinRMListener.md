---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 77cefdacfee2e2c8cb1e0d5508a418cf6bbafcbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569668"
---
# <span data-ttu-id="1b59c-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="1b59c-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="1b59c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b59c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b59c-103">Добавляет прослушиватель WinRM в VMSS.</span><span class="sxs-lookup"><span data-stu-id="1b59c-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b59c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b59c-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b59c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b59c-105">DESCRIPTION</span></span>
<span data-ttu-id="1b59c-106">Командлет **Add-AzureRmVmssWinRMListener** добавляет прослушиватель удаленного управления Windows (WinRM) в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1b59c-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1b59c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b59c-107">EXAMPLES</span></span>

### <span data-ttu-id="1b59c-108">Пример 1: Добавление прослушивателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="1b59c-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="1b59c-109">В этом примере в VMSS добавляется прослушиватель WinRM.</span><span class="sxs-lookup"><span data-stu-id="1b59c-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="1b59c-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1b59c-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="1b59c-111">Вторая команда добавляет прослушиватель HTTP протокола WinRM с сертификатом по указанному URL-адресу в VMSS.</span><span class="sxs-lookup"><span data-stu-id="1b59c-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="1b59c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b59c-112">PARAMETERS</span></span>

### <span data-ttu-id="1b59c-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1b59c-113">-CertificateUrl</span></span>
<span data-ttu-id="1b59c-114">Указывает ссылку (URL-адрес) сертификата, с помощью которого будут подготавливаться новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="1b59c-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="1b59c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b59c-115">-DefaultProfile</span></span>
<span data-ttu-id="1b59c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b59c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b59c-117">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1b59c-117">-Protocol</span></span>
<span data-ttu-id="1b59c-118">Задает протокол для прослушивателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="1b59c-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="1b59c-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1b59c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b59c-120">Через</span><span class="sxs-lookup"><span data-stu-id="1b59c-120">Http</span></span>
- <span data-ttu-id="1b59c-121">Протокол</span><span class="sxs-lookup"><span data-stu-id="1b59c-121">Https</span></span>

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

### <span data-ttu-id="1b59c-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b59c-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1b59c-123">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="1b59c-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="1b59c-124">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="1b59c-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="1b59c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b59c-125">-Confirm</span></span>
<span data-ttu-id="1b59c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b59c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b59c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b59c-127">-WhatIf</span></span>
<span data-ttu-id="1b59c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b59c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b59c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b59c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b59c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b59c-130">CommonParameters</span></span>
<span data-ttu-id="1b59c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b59c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b59c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b59c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b59c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b59c-133">INPUTS</span></span>

## <span data-ttu-id="1b59c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b59c-134">OUTPUTS</span></span>

### <span data-ttu-id="1b59c-135">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1b59c-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1b59c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b59c-136">NOTES</span></span>

## <span data-ttu-id="1b59c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b59c-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b59c-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1b59c-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


