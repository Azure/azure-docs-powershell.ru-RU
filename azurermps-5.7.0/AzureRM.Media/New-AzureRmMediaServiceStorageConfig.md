---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 7296d744749dd037c10d0d4d5ee2b0461a55b794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733040"
---
# <span data-ttu-id="f7820-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="f7820-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="f7820-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7820-102">SYNOPSIS</span></span>
<span data-ttu-id="f7820-103">Создайте конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f7820-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7820-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7820-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7820-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7820-105">DESCRIPTION</span></span>
<span data-ttu-id="f7820-106">Командлет **New-AzureRmMediaServiceStorageConfig** создает конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f7820-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="f7820-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7820-107">EXAMPLES</span></span>

### <span data-ttu-id="f7820-108">Пример 1: создание конфигурации учетной записи хранения для командлетов службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f7820-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="f7820-109">Первая команда создает объект учетной записи хранения с помощью командлета **New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="f7820-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="f7820-110">Команда называет эту учетную запись хранения Storage1 и тип с именем Standard_GRS и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f7820-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="f7820-111">Вторая команда создает объект конфигурации хранилища в качестве основной учетной записи хранилища, связанной со службой мультимедиа, с помощью ИДЕНТИФИКАЦИОНных данных учетной записи хранения, сохраненных в переменной $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f7820-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="f7820-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7820-112">PARAMETERS</span></span>

### <span data-ttu-id="f7820-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7820-113">-DefaultProfile</span></span>
<span data-ttu-id="f7820-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7820-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7820-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="f7820-115">-IsPrimary</span></span>
<span data-ttu-id="f7820-116">Указывает на то, что командлет создает учетную запись хранения в качестве основного хранилища для службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f7820-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7820-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f7820-117">-StorageAccountId</span></span>
<span data-ttu-id="f7820-118">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7820-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="f7820-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7820-119">-Confirm</span></span>
<span data-ttu-id="f7820-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7820-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7820-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7820-121">-WhatIf</span></span>
<span data-ttu-id="f7820-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7820-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7820-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7820-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7820-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7820-124">CommonParameters</span></span>
<span data-ttu-id="f7820-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7820-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7820-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7820-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7820-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7820-127">INPUTS</span></span>

### <span data-ttu-id="f7820-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7820-128">None</span></span>
<span data-ttu-id="f7820-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7820-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7820-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7820-130">OUTPUTS</span></span>

### <span data-ttu-id="f7820-131">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7820-131">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f7820-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7820-132">NOTES</span></span>

## <span data-ttu-id="f7820-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7820-133">RELATED LINKS</span></span>

[<span data-ttu-id="f7820-134">Sync (синхронизация) — AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="f7820-134">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


