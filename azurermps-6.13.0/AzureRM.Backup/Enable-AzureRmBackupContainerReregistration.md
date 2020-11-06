---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561167"
---
# <span data-ttu-id="52532-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="52532-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="52532-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52532-102">SYNOPSIS</span></span>
<span data-ttu-id="52532-103">Перерегистрация сервера для подключения к резервному хранилищу.</span><span class="sxs-lookup"><span data-stu-id="52532-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52532-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52532-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52532-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52532-105">DESCRIPTION</span></span>
<span data-ttu-id="52532-106">Командлет **Enable-AzureRmBackupContainerReregistration** перерегистрирует сервер для подключения к хранилищу архивации Azure и продолжит создание резервной копии цепочки точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="52532-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>
<span data-ttu-id="52532-107">Если вы уничтожаете сервер, все его облачные точки резервного копирования остаются в хранилище резервных копий.</span><span class="sxs-lookup"><span data-stu-id="52532-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="52532-108">Если вы создаете заменяемый сервер и присвойте ему полное доменное имя, вы можете подключить сервер к тому же хранилищу.</span><span class="sxs-lookup"><span data-stu-id="52532-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="52532-109">Этот командлет позволяет создавать резервные копии и добавлять новые точки резервного копирования в существующий комплект.</span><span class="sxs-lookup"><span data-stu-id="52532-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="52532-110">Новый сервер продолжает работать в цепочке резервных копий.</span><span class="sxs-lookup"><span data-stu-id="52532-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="52532-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52532-111">EXAMPLES</span></span>

## <span data-ttu-id="52532-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52532-112">PARAMETERS</span></span>

### <span data-ttu-id="52532-113">-Container</span><span class="sxs-lookup"><span data-stu-id="52532-113">-Container</span></span>
<span data-ttu-id="52532-114">Указывает контейнер, который перерегистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="52532-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="52532-115">Чтобы получить **AzureRmBackupContainer** , используйте командлет Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="52532-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52532-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52532-116">-DefaultProfile</span></span>
<span data-ttu-id="52532-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="52532-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52532-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52532-118">CommonParameters</span></span>
<span data-ttu-id="52532-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52532-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52532-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52532-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52532-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52532-121">INPUTS</span></span>

### <span data-ttu-id="52532-122">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="52532-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="52532-123">Параметры: Container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52532-123">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="52532-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52532-124">OUTPUTS</span></span>

### <span data-ttu-id="52532-125">System. void</span><span class="sxs-lookup"><span data-stu-id="52532-125">System.Void</span></span>

## <span data-ttu-id="52532-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="52532-126">NOTES</span></span>

## <span data-ttu-id="52532-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52532-127">RELATED LINKS</span></span>

[<span data-ttu-id="52532-128">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="52532-128">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="52532-129">Регистрация — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="52532-129">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


