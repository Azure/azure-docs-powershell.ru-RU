---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899646"
---
# <span data-ttu-id="0705b-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="0705b-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="0705b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0705b-102">SYNOPSIS</span></span>
<span data-ttu-id="0705b-103">Создайте конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0705b-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="0705b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0705b-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0705b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0705b-105">DESCRIPTION</span></span>
<span data-ttu-id="0705b-106">Командлет **New-AzMediaServiceStorageConfig** создает конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0705b-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="0705b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0705b-107">EXAMPLES</span></span>

### <span data-ttu-id="0705b-108">Пример 1: создание конфигурации учетной записи хранения для командлетов службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0705b-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="0705b-109">Первая команда создает объект учетной записи хранения с помощью командлета **New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="0705b-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="0705b-110">Команда называет эту учетную запись хранения Storage1 и тип с именем Standard_GRS и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="0705b-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="0705b-111">Вторая команда создает объект конфигурации хранилища в качестве основной учетной записи хранилища, связанной со службой мультимедиа, с помощью ИДЕНТИФИКАЦИОНных данных учетной записи хранения, сохраненных в переменной $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="0705b-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="0705b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0705b-112">PARAMETERS</span></span>

### <span data-ttu-id="0705b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0705b-113">-DefaultProfile</span></span>
<span data-ttu-id="0705b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0705b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0705b-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="0705b-115">-IsPrimary</span></span>
<span data-ttu-id="0705b-116">Указывает на то, что командлет создает учетную запись хранения в качестве основного хранилища для службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0705b-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0705b-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0705b-117">-StorageAccountId</span></span>
<span data-ttu-id="0705b-118">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0705b-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="0705b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0705b-119">-Confirm</span></span>
<span data-ttu-id="0705b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0705b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0705b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0705b-121">-WhatIf</span></span>
<span data-ttu-id="0705b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0705b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0705b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0705b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0705b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0705b-124">CommonParameters</span></span>
<span data-ttu-id="0705b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0705b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0705b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0705b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0705b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0705b-127">INPUTS</span></span>

### <span data-ttu-id="0705b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0705b-128">System.String</span></span>

## <span data-ttu-id="0705b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0705b-129">OUTPUTS</span></span>

### <span data-ttu-id="0705b-130">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0705b-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0705b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0705b-131">NOTES</span></span>

## <span data-ttu-id="0705b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0705b-132">RELATED LINKS</span></span>

[<span data-ttu-id="0705b-133">Sync (синхронизация) — AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="0705b-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)


