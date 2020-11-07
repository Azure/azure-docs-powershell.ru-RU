---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733587"
---
# <span data-ttu-id="8c2a7-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="8c2a7-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="8c2a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2a7-103">Загружает файл учетных данных хранилища для резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c2a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c2a7-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c2a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2a7-106">Командлет **Get-AzureRmBackupVaultCredentials** загружает файл учетных данных хранилища для резервного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="8c2a7-107">Функция резервного копирования использует файл учетных данных хранилища, чтобы подключить сервер к хранилищу резервных копий Azure и зарегистрировать его.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="8c2a7-108">Вы должны зарегистрировать сервер перед тем, как резервная копия сможет отправлять резервные данные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="8c2a7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c2a7-109">EXAMPLES</span></span>

## <span data-ttu-id="8c2a7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c2a7-110">PARAMETERS</span></span>

### <span data-ttu-id="8c2a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2a7-111">-DefaultProfile</span></span>
<span data-ttu-id="8c2a7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c2a7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c2a7-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="8c2a7-113">-TargetLocation</span></span>
<span data-ttu-id="8c2a7-114">Указывает конечный путь, по которому этот командлет хранит файл учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2a7-115">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="8c2a7-115">-Vault</span></span>
<span data-ttu-id="8c2a7-116">Указывает хранилище резервных копий, для которого этот командлет получает файл учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="8c2a7-117">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2a7-118">CommonParameters</span></span>
<span data-ttu-id="8c2a7-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2a7-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2a7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2a7-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c2a7-121">INPUTS</span></span>

### <span data-ttu-id="8c2a7-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="8c2a7-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="8c2a7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2a7-123">OUTPUTS</span></span>

### <span data-ttu-id="8c2a7-124">Подстрок</span><span class="sxs-lookup"><span data-stu-id="8c2a7-124">String</span></span>
<span data-ttu-id="8c2a7-125">Этот командлет возвращает имя файла учетных данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c2a7-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="8c2a7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c2a7-126">NOTES</span></span>

## <span data-ttu-id="8c2a7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c2a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c2a7-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8c2a7-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


