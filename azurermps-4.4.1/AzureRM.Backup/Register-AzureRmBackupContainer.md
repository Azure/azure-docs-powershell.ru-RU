---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565668"
---
# <span data-ttu-id="58391-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="58391-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="58391-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58391-102">SYNOPSIS</span></span>
<span data-ttu-id="58391-103">Регистрирует контейнер в хранилище резервных копий.</span><span class="sxs-lookup"><span data-stu-id="58391-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58391-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58391-104">SYNTAX</span></span>

### <span data-ttu-id="58391-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="58391-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58391-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="58391-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58391-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58391-107">DESCRIPTION</span></span>
<span data-ttu-id="58391-108">Командлет **Register-AzureRmBackupContainer** регистрирует контейнер в хранилище резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="58391-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="58391-109">Чтобы настроить архивацию с помощью резервной копии Azure, сначала Зарегистрируйте сервер или виртуальную машину в резервном хранилище.</span><span class="sxs-lookup"><span data-stu-id="58391-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="58391-110">Этот командлет регистрирует инфраструктуру в качестве виртуальной машины службы (IaaS) в указанном хранилище.</span><span class="sxs-lookup"><span data-stu-id="58391-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="58391-111">Операция регистрации связывает виртуальную машину Azure с резервным хранилищем и отслеживает виртуальную машину в течение жизненного цикла резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="58391-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="58391-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58391-112">EXAMPLES</span></span>

### <span data-ttu-id="58391-113">Пример 1: регистрация виртуальной машины в резервном хранилище</span><span class="sxs-lookup"><span data-stu-id="58391-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="58391-114">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="58391-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="58391-115">Команда хранит хранилище в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="58391-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="58391-116">Вторая команда регистрирует виртуальную машину с именем Contoso03Vm с хранилищем в $Vault.</span><span class="sxs-lookup"><span data-stu-id="58391-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="58391-117">Виртуальная машина принадлежит службе с именем ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="58391-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="58391-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58391-118">PARAMETERS</span></span>

### <span data-ttu-id="58391-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58391-119">-Name</span></span>
<span data-ttu-id="58391-120">Указывает имя виртуальной машины, зарегистрированной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="58391-120">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="58391-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58391-121">-ResourceGroupName</span></span>
<span data-ttu-id="58391-122">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="58391-122">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58391-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="58391-123">-ServiceName</span></span>
<span data-ttu-id="58391-124">Указывает имя службы виртуальной машины, зарегистрированной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="58391-124">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="58391-125">Обычно имя облачной службы имеет суффикс. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="58391-125">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="58391-126">Не включайте суффикс при указании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="58391-126">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="58391-127">Чтобы получить сведения о виртуальной машине, используйте командлет Get-AzureRMVM.</span><span class="sxs-lookup"><span data-stu-id="58391-127">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="58391-128">Имя службы — это свойство **DeploymentName** объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="58391-128">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58391-129">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="58391-129">-Vault</span></span>
<span data-ttu-id="58391-130">Указывает хранилище резервных копий, на которое этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="58391-130">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="58391-131">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="58391-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="58391-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58391-132">-DefaultProfile</span></span>
<span data-ttu-id="58391-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58391-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58391-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58391-134">CommonParameters</span></span>
<span data-ttu-id="58391-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58391-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58391-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58391-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58391-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58391-137">INPUTS</span></span>

### <span data-ttu-id="58391-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="58391-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="58391-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58391-139">OUTPUTS</span></span>

### <span data-ttu-id="58391-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="58391-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="58391-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="58391-141">NOTES</span></span>

## <span data-ttu-id="58391-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58391-142">RELATED LINKS</span></span>

[<span data-ttu-id="58391-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="58391-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


