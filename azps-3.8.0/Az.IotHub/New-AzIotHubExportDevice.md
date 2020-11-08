---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073817"
---
# <span data-ttu-id="94be5-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="94be5-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="94be5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94be5-102">SYNOPSIS</span></span>
<span data-ttu-id="94be5-103">Создает новое задание для экспорта устройств.</span><span class="sxs-lookup"><span data-stu-id="94be5-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="94be5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94be5-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94be5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94be5-105">DESCRIPTION</span></span>
<span data-ttu-id="94be5-106">Создает новое задание экспорта устройств для IotHub.</span><span class="sxs-lookup"><span data-stu-id="94be5-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="94be5-107">Все устройства будут экспортированы в указанный контейнер.</span><span class="sxs-lookup"><span data-stu-id="94be5-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="94be5-108">Обратитесь к следующей статье о том, как создать URI SAS.</span><span class="sxs-lookup"><span data-stu-id="94be5-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="94be5-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="94be5-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="94be5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94be5-110">EXAMPLES</span></span>

### <span data-ttu-id="94be5-111">Пример 1. выдать запрос на экспорт устройства.</span><span class="sxs-lookup"><span data-stu-id="94be5-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="94be5-112">Создает новый запрос на экспорт устройства для IotHub "myiothub", исключая ключи.</span><span class="sxs-lookup"><span data-stu-id="94be5-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="94be5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94be5-113">PARAMETERS</span></span>

### <span data-ttu-id="94be5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94be5-114">-DefaultProfile</span></span>
<span data-ttu-id="94be5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94be5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94be5-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="94be5-116">-ExcludeKeys</span></span>
<span data-ttu-id="94be5-117">Позволяет экспортировать устройства без ключей.</span><span class="sxs-lookup"><span data-stu-id="94be5-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94be5-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="94be5-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="94be5-119">Универсальный код ресурса (URI) для экспорта большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="94be5-119">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94be5-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94be5-120">-Name</span></span>
<span data-ttu-id="94be5-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="94be5-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94be5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94be5-122">-ResourceGroupName</span></span>
<span data-ttu-id="94be5-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="94be5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="94be5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94be5-124">-Confirm</span></span>
<span data-ttu-id="94be5-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94be5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94be5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94be5-126">-WhatIf</span></span>
<span data-ttu-id="94be5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94be5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94be5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94be5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94be5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94be5-129">CommonParameters</span></span>
<span data-ttu-id="94be5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94be5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94be5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94be5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94be5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94be5-132">INPUTS</span></span>

### <span data-ttu-id="94be5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="94be5-133">System.String</span></span>

## <span data-ttu-id="94be5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94be5-134">OUTPUTS</span></span>

### <span data-ttu-id="94be5-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="94be5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="94be5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="94be5-136">NOTES</span></span>

## <span data-ttu-id="94be5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94be5-137">RELATED LINKS</span></span>
