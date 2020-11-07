---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 3de18d5d7cc1c3525f1526beb5dd7337175eb041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735123"
---
# <span data-ttu-id="04301-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="04301-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04301-102">SYNOPSIS</span></span>
<span data-ttu-id="04301-103">Восстанавливает службу управления API из указанного блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04301-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04301-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04301-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04301-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04301-105">DESCRIPTION</span></span>
<span data-ttu-id="04301-106">Командлет **RESTORE-AzureRmApiManagement** восстанавливает службу управления API из указанного резервного копирования, расположенного в большом двоичном объекте Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="04301-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="04301-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04301-107">EXAMPLES</span></span>

### <span data-ttu-id="04301-108">Пример 1: восстановление службы управления API</span><span class="sxs-lookup"><span data-stu-id="04301-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="04301-109">Эта команда восстанавливает службу управления API из большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04301-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="04301-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04301-110">PARAMETERS</span></span>

### <span data-ttu-id="04301-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04301-111">-DefaultProfile</span></span>
<span data-ttu-id="04301-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04301-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="04301-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04301-113">-Name</span></span>
<span data-ttu-id="04301-114">Указывает имя экземпляра управления API, который будет восстановлен вместе с резервной копией.</span><span class="sxs-lookup"><span data-stu-id="04301-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04301-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04301-115">-PassThru</span></span>
<span data-ttu-id="04301-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="04301-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04301-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="04301-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04301-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04301-118">-ResourceGroupName</span></span>
<span data-ttu-id="04301-119">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="04301-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04301-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="04301-120">-SourceBlobName</span></span>
<span data-ttu-id="04301-121">Указывает имя блоба источника резервного копирования хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04301-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04301-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="04301-122">-SourceContainerName</span></span>
<span data-ttu-id="04301-123">Указывает имя контейнера источника резервной копии хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04301-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04301-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="04301-124">-StorageContext</span></span>
<span data-ttu-id="04301-125">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="04301-125">Specifies the storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04301-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04301-126">CommonParameters</span></span>
<span data-ttu-id="04301-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04301-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04301-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04301-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04301-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04301-129">INPUTS</span></span>

### <span data-ttu-id="04301-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="04301-130">None</span></span>
<span data-ttu-id="04301-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="04301-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04301-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04301-132">OUTPUTS</span></span>

### <span data-ttu-id="04301-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="04301-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="04301-134">NOTES</span></span>

## <span data-ttu-id="04301-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04301-135">RELATED LINKS</span></span>

[<span data-ttu-id="04301-136">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-136">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="04301-137">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-137">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="04301-138">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-138">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="04301-139">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="04301-139">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


