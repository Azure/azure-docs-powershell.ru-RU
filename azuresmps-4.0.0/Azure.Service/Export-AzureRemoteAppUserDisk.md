---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075678"
---
# <span data-ttu-id="c52e4-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c52e4-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="c52e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c52e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c52e4-103">Экспортируются все диски пользователей из одной коллекции Azure RemoteApp в указанную учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="c52e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c52e4-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c52e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52e4-105">DESCRIPTION</span></span>
<span data-ttu-id="c52e4-106">Командлет **Export-AzureRemoteAppUserDisk** экспортирует все диски пользователей из одной коллекции RemoteApp Azure в указанную учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="c52e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c52e4-107">EXAMPLES</span></span>

### <span data-ttu-id="c52e4-108">Пример 1: экспорт всех дисков пользователей из коллекции в указанную учетную запись хранения Azure</span><span class="sxs-lookup"><span data-stu-id="c52e4-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="c52e4-109">Эта команда экспортирует все диски пользователей из коллекции Contoso в контейнер с именем ContainerName в указанной учетной записи хранения Azure с именем AccountName и ключом AccountKey.</span><span class="sxs-lookup"><span data-stu-id="c52e4-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="c52e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c52e4-110">PARAMETERS</span></span>

### <span data-ttu-id="c52e4-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c52e4-111">-CollectionName</span></span>
<span data-ttu-id="c52e4-112">Указывает имя исходной коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="c52e4-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="c52e4-114">Указывает имя контейнера в конечной учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c52e4-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="c52e4-116">Задает ключ учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-116">Specifies the Key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c52e4-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="c52e4-118">Указывает имя целевой учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c52e4-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="c52e4-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="c52e4-120">Указывает на то, что командлет перезапишет существующий диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="c52e4-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c52e4-121">-Profile</span></span>
<span data-ttu-id="c52e4-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c52e4-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c52e4-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c52e4-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52e4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c52e4-124">-Confirm</span></span>
<span data-ttu-id="c52e4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c52e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52e4-126">-WhatIf</span></span>
<span data-ttu-id="c52e4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c52e4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c52e4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c52e4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52e4-129">CommonParameters</span></span>
<span data-ttu-id="c52e4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c52e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52e4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52e4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c52e4-132">INPUTS</span></span>

## <span data-ttu-id="c52e4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52e4-133">OUTPUTS</span></span>

## <span data-ttu-id="c52e4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c52e4-134">NOTES</span></span>

## <span data-ttu-id="c52e4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c52e4-135">RELATED LINKS</span></span>

[<span data-ttu-id="c52e4-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c52e4-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="c52e4-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c52e4-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


