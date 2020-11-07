---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
ms.openlocfilehash: dd9c13298adac34a53ed2f97bbc1e3edc95892df
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913693"
---
# <span data-ttu-id="f3bc0-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="f3bc0-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="f3bc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bc0-103">Добавляет прослушиватель WinRM в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3bc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3bc0-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3bc0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="f3bc0-106">Командлет **Add-AzureRmVmssWinRMListener** добавляет прослушиватель удаленного управления Windows (WinRM) в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f3bc0-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f3bc0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3bc0-107">EXAMPLES</span></span>

### <span data-ttu-id="f3bc0-108">Пример 1: Добавление прослушивателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="f3bc0-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="f3bc0-109">В этом примере в VMSS добавляется прослушиватель WinRM.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="f3bc0-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="f3bc0-111">Вторая команда добавляет прослушиватель HTTP протокола WinRM с сертификатом по указанному URL-адресу в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="f3bc0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3bc0-112">PARAMETERS</span></span>

### <span data-ttu-id="f3bc0-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f3bc0-113">-CertificateUrl</span></span>
<span data-ttu-id="f3bc0-114">Указывает ссылку (URL-адрес) сертификата, с помощью которого будут подготавливаться новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="f3bc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bc0-115">-DefaultProfile</span></span>
<span data-ttu-id="f3bc0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3bc0-117">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f3bc0-117">-Protocol</span></span>
<span data-ttu-id="f3bc0-118">Задает протокол для прослушивателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="f3bc0-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f3bc0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3bc0-120">Через</span><span class="sxs-lookup"><span data-stu-id="f3bc0-120">Http</span></span>
- <span data-ttu-id="f3bc0-121">Протокол</span><span class="sxs-lookup"><span data-stu-id="f3bc0-121">Https</span></span>

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

### <span data-ttu-id="f3bc0-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f3bc0-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f3bc0-123">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="f3bc0-124">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bc0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3bc0-125">-Confirm</span></span>
<span data-ttu-id="f3bc0-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3bc0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bc0-127">-WhatIf</span></span>
<span data-ttu-id="f3bc0-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3bc0-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3bc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bc0-130">CommonParameters</span></span>
<span data-ttu-id="f3bc0-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bc0-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3bc0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bc0-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3bc0-133">INPUTS</span></span>

### <span data-ttu-id="f3bc0-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f3bc0-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f3bc0-135">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f3bc0-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3bc0-136">OUTPUTS</span></span>

### <span data-ttu-id="f3bc0-137">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f3bc0-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3bc0-138">NOTES</span></span>

## <span data-ttu-id="f3bc0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3bc0-139">RELATED LINKS</span></span>

[<span data-ttu-id="f3bc0-140">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f3bc0-140">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


