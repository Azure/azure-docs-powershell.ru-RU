---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: e9d413a8f77422b723c2dabc57d7d68c691617d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720361"
---
# <span data-ttu-id="69bdb-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="69bdb-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="69bdb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="69bdb-103">Синхронизирует ключи учетной записи хранения, связанные с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69bdb-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="69bdb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69bdb-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69bdb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="69bdb-106">Командлет **Sync-AzMediaServiceStorageKey** синхронизирует ключи учетной записи хранения, связанные с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69bdb-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="69bdb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="69bdb-108">Пример 1: Синхронизация ключей учетной записи хранения, связанной с службой мультимедиа</span><span class="sxs-lookup"><span data-stu-id="69bdb-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="69bdb-109">Первая команда использует командлет Get-AzStorageAccount для получения учетной записи хранения с именем Storage135, которая принадлежит к ResourceGroup001, и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="69bdb-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="69bdb-110">Вторая команда синхронизирует ключи учетной записи хранения для службы мультимедиа с именем MediaService001, используя свойство **ID** , содержащееся в переменной $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="69bdb-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="69bdb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69bdb-111">PARAMETERS</span></span>

### <span data-ttu-id="69bdb-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="69bdb-112">-AccountName</span></span>
<span data-ttu-id="69bdb-113">Указывает имя службы мультимедиа, которую синхронизируется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69bdb-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="69bdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bdb-114">-DefaultProfile</span></span>
<span data-ttu-id="69bdb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69bdb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69bdb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bdb-116">-ResourceGroupName</span></span>
<span data-ttu-id="69bdb-117">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69bdb-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="69bdb-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="69bdb-118">-StorageAccountId</span></span>
<span data-ttu-id="69bdb-119">Указывает идентификатор учетной записи хранения, связанный с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69bdb-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="69bdb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69bdb-120">-Confirm</span></span>
<span data-ttu-id="69bdb-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69bdb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bdb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bdb-122">-WhatIf</span></span>
<span data-ttu-id="69bdb-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69bdb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bdb-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69bdb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bdb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bdb-125">CommonParameters</span></span>
<span data-ttu-id="69bdb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69bdb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bdb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bdb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bdb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69bdb-128">INPUTS</span></span>

### <span data-ttu-id="69bdb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="69bdb-129">System.String</span></span>

## <span data-ttu-id="69bdb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69bdb-130">OUTPUTS</span></span>

### <span data-ttu-id="69bdb-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69bdb-131">System.Boolean</span></span>

## <span data-ttu-id="69bdb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="69bdb-132">NOTES</span></span>

## <span data-ttu-id="69bdb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69bdb-133">RELATED LINKS</span></span>
