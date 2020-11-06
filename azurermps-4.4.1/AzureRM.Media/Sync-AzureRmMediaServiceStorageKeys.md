---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 71112bf54f4de8e0c7e4fd1ecfd296eff45ac868
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568048"
---
# <span data-ttu-id="1441c-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="1441c-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="1441c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1441c-102">SYNOPSIS</span></span>
<span data-ttu-id="1441c-103">Синхронизирует ключи учетной записи хранения, связанные с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1441c-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1441c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1441c-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1441c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1441c-105">DESCRIPTION</span></span>
<span data-ttu-id="1441c-106">Командлет **Sync-AzureRmMediaServiceStorageKeys** синхронизирует ключи учетной записи хранения, связанные с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1441c-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="1441c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1441c-107">EXAMPLES</span></span>

### <span data-ttu-id="1441c-108">Пример 1: Синхронизация ключей учетной записи хранения, связанной с службой мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1441c-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="1441c-109">Первая команда использует командлет Get-AzureRmStorageAccount для получения учетной записи хранения с именем Storage135, которая принадлежит к ResourceGroup001, и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1441c-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="1441c-110">Вторая команда синхронизирует ключи учетной записи хранения для службы мультимедиа с именем MediaService001, используя свойство **ID** , содержащееся в переменной $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1441c-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="1441c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1441c-111">PARAMETERS</span></span>

### <span data-ttu-id="1441c-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="1441c-112">-AccountName</span></span>
<span data-ttu-id="1441c-113">Указывает имя службы мультимедиа, которую синхронизируется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1441c-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="1441c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1441c-114">-ResourceGroupName</span></span>
<span data-ttu-id="1441c-115">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1441c-115">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1441c-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1441c-116">-StorageAccountId</span></span>
<span data-ttu-id="1441c-117">Указывает идентификатор учетной записи хранения, связанный с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1441c-117">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="1441c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1441c-118">-Confirm</span></span>
<span data-ttu-id="1441c-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1441c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1441c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1441c-120">-WhatIf</span></span>
<span data-ttu-id="1441c-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1441c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1441c-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1441c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1441c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1441c-123">-DefaultProfile</span></span>
<span data-ttu-id="1441c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1441c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1441c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1441c-125">CommonParameters</span></span>
<span data-ttu-id="1441c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1441c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1441c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1441c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1441c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1441c-128">INPUTS</span></span>

## <span data-ttu-id="1441c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1441c-129">OUTPUTS</span></span>

### <span data-ttu-id="1441c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1441c-130">System.Boolean</span></span>

## <span data-ttu-id="1441c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1441c-131">NOTES</span></span>

## <span data-ttu-id="1441c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1441c-132">RELATED LINKS</span></span>

