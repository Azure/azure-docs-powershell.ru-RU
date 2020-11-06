---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: b208602532428d14c2af1504c5b8af2cce0b155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560516"
---
# <span data-ttu-id="fe0ef-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="fe0ef-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="fe0ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0ef-103">Загружает файл учетных данных хранилища для резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe0ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe0ef-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe0ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe0ef-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0ef-106">Командлет **Get-AzureRmBackupVaultCredentials** загружает файл учетных данных хранилища для резервного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="fe0ef-107">Функция резервного копирования использует файл учетных данных хранилища, чтобы подключить сервер к хранилищу резервных копий Azure и зарегистрировать его.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="fe0ef-108">Вы должны зарегистрировать сервер перед тем, как резервная копия сможет отправлять резервные данные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="fe0ef-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe0ef-109">EXAMPLES</span></span>

## <span data-ttu-id="fe0ef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe0ef-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0ef-111">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="fe0ef-111">-TargetLocation</span></span>
<span data-ttu-id="fe0ef-112">Указывает конечный путь, по которому этот командлет хранит файл учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-112">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

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

### <span data-ttu-id="fe0ef-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="fe0ef-113">-Vault</span></span>
<span data-ttu-id="fe0ef-114">Указывает хранилище резервных копий, для которого этот командлет получает файл учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-114">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="fe0ef-115">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-115">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0ef-116">-DefaultProfile</span></span>
<span data-ttu-id="fe0ef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0ef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0ef-118">CommonParameters</span></span>
<span data-ttu-id="fe0ef-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0ef-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0ef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0ef-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe0ef-121">INPUTS</span></span>

### <span data-ttu-id="fe0ef-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="fe0ef-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="fe0ef-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe0ef-123">OUTPUTS</span></span>

### <span data-ttu-id="fe0ef-124">Подстрок</span><span class="sxs-lookup"><span data-stu-id="fe0ef-124">String</span></span>
<span data-ttu-id="fe0ef-125">Этот командлет возвращает имя файла учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe0ef-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="fe0ef-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe0ef-126">NOTES</span></span>

## <span data-ttu-id="fe0ef-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe0ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="fe0ef-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="fe0ef-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


