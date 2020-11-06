---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567177"
---
# <span data-ttu-id="d4883-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d4883-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="d4883-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4883-102">SYNOPSIS</span></span>
<span data-ttu-id="d4883-103">Изменяет тип хранилища резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d4883-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4883-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4883-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4883-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4883-105">DESCRIPTION</span></span>
<span data-ttu-id="d4883-106">Командлет **Set-AzureRmBackupVault** изменяет тип хранилища для хранилища резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4883-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="d4883-107">Изменить другие свойства хранилища нельзя.</span><span class="sxs-lookup"><span data-stu-id="d4883-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="d4883-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4883-108">EXAMPLES</span></span>

### <span data-ttu-id="d4883-109">Пример 1: изменение хранилища для существующего хранилища</span><span class="sxs-lookup"><span data-stu-id="d4883-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="d4883-110">Эта команда получает хранилище резервных копий Azure с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="d4883-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="d4883-111">Команда передает это хранилище в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d4883-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d4883-112">Текущий командлет изменяет тип хранилища на LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="d4883-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="d4883-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4883-113">PARAMETERS</span></span>

### <span data-ttu-id="d4883-114">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="d4883-114">-Storage</span></span>
<span data-ttu-id="d4883-115">Указывает тип хранения архивных данных.</span><span class="sxs-lookup"><span data-stu-id="d4883-115">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="d4883-116">Допустимые значения этого параметра: LocallyRedundant и геоизбыточный.</span><span class="sxs-lookup"><span data-stu-id="d4883-116">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4883-117">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="d4883-117">-Vault</span></span>
<span data-ttu-id="d4883-118">Указывает хранилище резервных копий, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d4883-118">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="d4883-119">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="d4883-119">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="d4883-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4883-120">-DefaultProfile</span></span>
<span data-ttu-id="d4883-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4883-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4883-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4883-122">CommonParameters</span></span>
<span data-ttu-id="d4883-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4883-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4883-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4883-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4883-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4883-125">INPUTS</span></span>

### <span data-ttu-id="d4883-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d4883-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="d4883-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4883-127">OUTPUTS</span></span>

### <span data-ttu-id="d4883-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4883-128">None</span></span>

## <span data-ttu-id="d4883-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4883-129">NOTES</span></span>
* <span data-ttu-id="d4883-130">При регистрации первого сервера или виртуальной машины для хранилища этот тип хранения заблокирован.</span><span class="sxs-lookup"><span data-stu-id="d4883-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="d4883-131">Впоследствии изменить тип хранилища нельзя.</span><span class="sxs-lookup"><span data-stu-id="d4883-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="d4883-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4883-132">RELATED LINKS</span></span>

[<span data-ttu-id="d4883-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d4883-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="d4883-134">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d4883-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="d4883-135">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d4883-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


