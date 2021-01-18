---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520019"
---
# <span data-ttu-id="17b4d-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="17b4d-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="17b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="17b4d-103">Синхронизирует ключи учетной записи хранения для учетной записи хранения, связанной со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="17b4d-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="17b4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17b4d-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17b4d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="17b4d-106">Командалет **Sync-AzMediaServiceStorageKey** синхронизирует ключи учетной записи хранения для учетной записи хранения, связанной со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="17b4d-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="17b4d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="17b4d-108">Пример 1. Синхронизация ключей учетной записи хранения для учетной записи хранения, связанной со службой мультимедиа</span><span class="sxs-lookup"><span data-stu-id="17b4d-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="17b4d-109">Первая команда использует Get-AzStorageAccount для получения учетной записи хранения "Хранилище135", которая принадлежит к ResourceGroup001, и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="17b4d-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="17b4d-110">Вторая команда синхронизирует ключи учетной записи хранения для службы мультимедиа MediaService001, используя свойство **ID,** содержа $StorageAccount переменной.</span><span class="sxs-lookup"><span data-stu-id="17b4d-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="17b4d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17b4d-111">PARAMETERS</span></span>

### <span data-ttu-id="17b4d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17b4d-112">-AccountName</span></span>
<span data-ttu-id="17b4d-113">Указывает имя службы мультимедиа, которая синхронизируется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b4d-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b4d-114">-DefaultProfile</span></span>
<span data-ttu-id="17b4d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17b4d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17b4d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b4d-116">-ResourceGroupName</span></span>
<span data-ttu-id="17b4d-117">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="17b4d-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="17b4d-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="17b4d-118">-StorageAccountId</span></span>
<span data-ttu-id="17b4d-119">Определяет ИД учетной записи хранения, связанный с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="17b4d-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b4d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17b4d-120">-Confirm</span></span>
<span data-ttu-id="17b4d-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="17b4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b4d-122">-WhatIf</span></span>
<span data-ttu-id="17b4d-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b4d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b4d-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17b4d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b4d-125">CommonParameters</span></span>
<span data-ttu-id="17b4d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b4d-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b4d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b4d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17b4d-128">INPUTS</span></span>

### <span data-ttu-id="17b4d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="17b4d-129">System.String</span></span>

## <span data-ttu-id="17b4d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17b4d-130">OUTPUTS</span></span>

### <span data-ttu-id="17b4d-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17b4d-131">System.Boolean</span></span>

## <span data-ttu-id="17b4d-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17b4d-132">NOTES</span></span>

## <span data-ttu-id="17b4d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17b4d-133">RELATED LINKS</span></span>
