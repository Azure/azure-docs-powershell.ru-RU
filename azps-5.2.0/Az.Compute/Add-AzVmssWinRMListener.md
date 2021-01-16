---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392207"
---
# <span data-ttu-id="09c54-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="09c54-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="09c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c54-102">SYNOPSIS</span></span>
<span data-ttu-id="09c54-103">Добавляет в VMSS слушателя WinRM.</span><span class="sxs-lookup"><span data-stu-id="09c54-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="09c54-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="09c54-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09c54-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09c54-105">DESCRIPTION</span></span>
<span data-ttu-id="09c54-106">В наборе виртуальных машин (VMSS) Windows Remote Management **-AzVmssWinRMListener** добавляется слушатель Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="09c54-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="09c54-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="09c54-107">EXAMPLES</span></span>

### <span data-ttu-id="09c54-108">Пример 1. Добавление слушателя WinRM в VMSS</span><span class="sxs-lookup"><span data-stu-id="09c54-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="09c54-109">В этом примере в VMSS добавляется слушатель WinRM.</span><span class="sxs-lookup"><span data-stu-id="09c54-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="09c54-110">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09c54-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="09c54-111">Вторая команда добавляет в VMSS прослушки HTTP-протокола WinRM с сертификатом по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="09c54-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="09c54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09c54-112">PARAMETERS</span></span>

### <span data-ttu-id="09c54-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="09c54-113">-CertificateUrl</span></span>
<span data-ttu-id="09c54-114">Указывает ссылку (в качестве URL-адреса) сертификата, с помощью которого можно получить новые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="09c54-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="09c54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c54-115">-DefaultProfile</span></span>
<span data-ttu-id="09c54-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09c54-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09c54-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="09c54-117">-Protocol</span></span>
<span data-ttu-id="09c54-118">Определяет протокол для прослушки WinRM.</span><span class="sxs-lookup"><span data-stu-id="09c54-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="09c54-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="09c54-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09c54-120">Http</span><span class="sxs-lookup"><span data-stu-id="09c54-120">Http</span></span>
- <span data-ttu-id="09c54-121">Https</span><span class="sxs-lookup"><span data-stu-id="09c54-121">Https</span></span>

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

### <span data-ttu-id="09c54-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09c54-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09c54-123">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="09c54-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="09c54-124">Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="09c54-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="09c54-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09c54-125">-Confirm</span></span>
<span data-ttu-id="09c54-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09c54-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c54-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c54-127">-WhatIf</span></span>
<span data-ttu-id="09c54-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09c54-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09c54-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="09c54-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c54-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c54-130">CommonParameters</span></span>
<span data-ttu-id="09c54-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c54-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c54-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09c54-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c54-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09c54-133">INPUTS</span></span>

### <span data-ttu-id="09c54-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="09c54-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="09c54-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="09c54-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="09c54-136">System.String</span><span class="sxs-lookup"><span data-stu-id="09c54-136">System.String</span></span>

## <span data-ttu-id="09c54-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09c54-137">OUTPUTS</span></span>

### <span data-ttu-id="09c54-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="09c54-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="09c54-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="09c54-139">NOTES</span></span>

## <span data-ttu-id="09c54-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09c54-140">RELATED LINKS</span></span>

[<span data-ttu-id="09c54-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="09c54-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


