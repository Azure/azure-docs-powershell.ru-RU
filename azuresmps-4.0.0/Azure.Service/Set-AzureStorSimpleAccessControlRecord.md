---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075858"
---
# <span data-ttu-id="e6c20-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e6c20-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="e6c20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6c20-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c20-103">Обновляет IQN записи контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="e6c20-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="e6c20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6c20-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6c20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6c20-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c20-106">Командлет **Set-AzureStorSimpleAccessControlRecord** обновляет полное имя iSCSI (IQN) существующей записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e6c20-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="e6c20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6c20-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c20-108">Пример 1: Обновление записи контроля доступа</span><span class="sxs-lookup"><span data-stu-id="e6c20-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="e6c20-109">Эта команда обновляет запись контроля доступа с именем Acr10 для инициатора iSCSI с именем IqnUpdated.</span><span class="sxs-lookup"><span data-stu-id="e6c20-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="e6c20-110">Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="e6c20-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="e6c20-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6c20-111">PARAMETERS</span></span>

### <span data-ttu-id="e6c20-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="e6c20-112">-ACRName</span></span>
<span data-ttu-id="e6c20-113">Указывает имя записи управления доступом, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="e6c20-113">Specifies a name of the access control record to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c20-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="e6c20-114">-IQNInitiatorName</span></span>
<span data-ttu-id="e6c20-115">Указывает IQN инициатора iSCSI, которому этот командлет предоставляет доступ к тому.</span><span class="sxs-lookup"><span data-stu-id="e6c20-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c20-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="e6c20-116">-NewName</span></span>
<span data-ttu-id="e6c20-117">Задает новое имя записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e6c20-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c20-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6c20-118">-Profile</span></span>
<span data-ttu-id="e6c20-119">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c20-119">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c20-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e6c20-120">-WaitForComplete</span></span>
<span data-ttu-id="e6c20-121">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6c20-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e6c20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c20-122">CommonParameters</span></span>
<span data-ttu-id="e6c20-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6c20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c20-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c20-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c20-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6c20-125">INPUTS</span></span>

### <span data-ttu-id="e6c20-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6c20-126">None</span></span>

## <span data-ttu-id="e6c20-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6c20-127">OUTPUTS</span></span>

### <span data-ttu-id="e6c20-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="e6c20-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="e6c20-129">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e6c20-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e6c20-130">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e6c20-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="e6c20-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6c20-131">NOTES</span></span>

## <span data-ttu-id="e6c20-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6c20-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6c20-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e6c20-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e6c20-134">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e6c20-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e6c20-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e6c20-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


