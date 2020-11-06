---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557567"
---
# <span data-ttu-id="1eb8d-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="1eb8d-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="1eb8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb8d-103">Добавляет прослушиватель WinRM в VMSS.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eb8d-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb8d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb8d-106">Командлет **Add-AzureRmVmssWinRMListener** добавляет прослушиватель удаленного управления Windows (WinRM) в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1eb8d-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1eb8d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-107">EXAMPLES</span></span>

### <span data-ttu-id="1eb8d-108">Пример 1: Добавление прослушивателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="1eb8d-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="1eb8d-109">В этом примере в VMSS добавляется прослушиватель WinRM.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="1eb8d-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="1eb8d-111">Вторая команда добавляет прослушиватель HTTP протокола WinRM с сертификатом по указанному URL-адресу в VMSS.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="1eb8d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-112">PARAMETERS</span></span>

### <span data-ttu-id="1eb8d-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1eb8d-113">-CertificateUrl</span></span>
<span data-ttu-id="1eb8d-114">Указывает ссылку (URL-адрес) сертификата, с помощью которого будут подготавливаться новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8d-115">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1eb8d-115">-Protocol</span></span>
<span data-ttu-id="1eb8d-116">Задает протокол для прослушивателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="1eb8d-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1eb8d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1eb8d-118">Через</span><span class="sxs-lookup"><span data-stu-id="1eb8d-118">Http</span></span>
- <span data-ttu-id="1eb8d-119">Протокол</span><span class="sxs-lookup"><span data-stu-id="1eb8d-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8d-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1eb8d-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1eb8d-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="1eb8d-122">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb8d-123">-Confirm</span></span>
<span data-ttu-id="1eb8d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb8d-125">-WhatIf</span></span>
<span data-ttu-id="1eb8d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1eb8d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb8d-128">CommonParameters</span></span>
<span data-ttu-id="1eb8d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb8d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb8d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb8d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eb8d-131">INPUTS</span></span>

### <span data-ttu-id="1eb8d-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="1eb8d-132">None</span></span>
<span data-ttu-id="1eb8d-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1eb8d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-134">OUTPUTS</span></span>

### <span data-ttu-id="1eb8d-135">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1eb8d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eb8d-136">NOTES</span></span>

## <span data-ttu-id="1eb8d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1eb8d-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1eb8d-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


