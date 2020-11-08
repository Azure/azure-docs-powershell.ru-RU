---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066596"
---
# <span data-ttu-id="61ccc-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="61ccc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="61ccc-103">Восстанавливает службу управления API из указанного блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61ccc-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="61ccc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61ccc-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ccc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="61ccc-106">Командлет **RESTORE-AzApiManagement** восстанавливает службу управления API из указанного резервного копирования, расположенного в большом двоичном объекте Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="61ccc-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="61ccc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61ccc-107">EXAMPLES</span></span>

### <span data-ttu-id="61ccc-108">Пример 1: восстановление службы управления API</span><span class="sxs-lookup"><span data-stu-id="61ccc-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="61ccc-109">Эта команда восстанавливает службу управления API из большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61ccc-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="61ccc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61ccc-110">PARAMETERS</span></span>

### <span data-ttu-id="61ccc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ccc-111">-DefaultProfile</span></span>
<span data-ttu-id="61ccc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61ccc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61ccc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61ccc-113">-Name</span></span>
<span data-ttu-id="61ccc-114">Указывает имя экземпляра управления API, который будет восстановлен вместе с резервной копией.</span><span class="sxs-lookup"><span data-stu-id="61ccc-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ccc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ccc-115">-PassThru</span></span>
<span data-ttu-id="61ccc-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="61ccc-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61ccc-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="61ccc-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61ccc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ccc-118">-ResourceGroupName</span></span>
<span data-ttu-id="61ccc-119">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="61ccc-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ccc-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="61ccc-120">-SourceBlobName</span></span>
<span data-ttu-id="61ccc-121">Указывает имя блоба источника резервного копирования хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61ccc-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ccc-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="61ccc-122">-SourceContainerName</span></span>
<span data-ttu-id="61ccc-123">Указывает имя контейнера источника резервной копии хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61ccc-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ccc-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="61ccc-124">-StorageContext</span></span>
<span data-ttu-id="61ccc-125">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="61ccc-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ccc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ccc-126">CommonParameters</span></span>
<span data-ttu-id="61ccc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61ccc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ccc-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61ccc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ccc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61ccc-129">INPUTS</span></span>

### <span data-ttu-id="61ccc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61ccc-130">System.String</span></span>

## <span data-ttu-id="61ccc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ccc-131">OUTPUTS</span></span>

### <span data-ttu-id="61ccc-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="61ccc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="61ccc-133">NOTES</span></span>

## <span data-ttu-id="61ccc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61ccc-134">RELATED LINKS</span></span>

[<span data-ttu-id="61ccc-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="61ccc-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="61ccc-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="61ccc-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61ccc-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


