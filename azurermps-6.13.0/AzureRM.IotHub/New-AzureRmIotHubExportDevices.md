---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 4c13a6366f0ccae803e8020f16bf2b566bd70934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565423"
---
# <span data-ttu-id="0ea09-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="0ea09-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="0ea09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ea09-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea09-103">Создает новое задание для экспорта устройств.</span><span class="sxs-lookup"><span data-stu-id="0ea09-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ea09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ea09-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ea09-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea09-106">Создает новое задание экспорта устройств для IotHub.</span><span class="sxs-lookup"><span data-stu-id="0ea09-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="0ea09-107">Все устройства будут экспортированы в указанный контейнер.</span><span class="sxs-lookup"><span data-stu-id="0ea09-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="0ea09-108">Обратитесь к следующей статье о том, как создать URI SAS.</span><span class="sxs-lookup"><span data-stu-id="0ea09-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="0ea09-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="0ea09-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="0ea09-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ea09-110">EXAMPLES</span></span>

### <span data-ttu-id="0ea09-111">Пример 1. выдать запрос на экспорт устройства.</span><span class="sxs-lookup"><span data-stu-id="0ea09-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="0ea09-112">Создает новый запрос на экспорт устройства для IotHub "myiothub", исключая ключи.</span><span class="sxs-lookup"><span data-stu-id="0ea09-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="0ea09-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ea09-113">PARAMETERS</span></span>

### <span data-ttu-id="0ea09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea09-114">-DefaultProfile</span></span>
<span data-ttu-id="0ea09-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0ea09-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ea09-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="0ea09-116">-ExcludeKeys</span></span>
<span data-ttu-id="0ea09-117">Позволяет экспортировать устройства без ключей.</span><span class="sxs-lookup"><span data-stu-id="0ea09-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="0ea09-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0ea09-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="0ea09-119">Универсальный код ресурса (URI) для экспорта большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea09-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="0ea09-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ea09-120">-Name</span></span>
<span data-ttu-id="0ea09-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="0ea09-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="0ea09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea09-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ea09-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0ea09-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0ea09-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ea09-124">-Confirm</span></span>
<span data-ttu-id="0ea09-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ea09-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea09-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea09-126">-WhatIf</span></span>
<span data-ttu-id="0ea09-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ea09-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea09-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ea09-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea09-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea09-129">CommonParameters</span></span>
<span data-ttu-id="0ea09-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ea09-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea09-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea09-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea09-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ea09-132">INPUTS</span></span>

### <span data-ttu-id="0ea09-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ea09-133">System.String</span></span>

## <span data-ttu-id="0ea09-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ea09-134">OUTPUTS</span></span>

### <span data-ttu-id="0ea09-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="0ea09-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="0ea09-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ea09-136">NOTES</span></span>

## <span data-ttu-id="0ea09-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ea09-137">RELATED LINKS</span></span>
